KLASS_NAME_DEFAULT = 'KlassName'
FILE_NAME_DEFAULT = 'klass_name'

LIB_TEMPLATE =
"class #{KLASS_NAME_DEFAULT}
end"

SPEC_TEMPLATE =
"require '#{FILE_NAME_DEFAULT}'

describe #{KLASS_NAME_DEFAULT} do
  it 'works!' do
    subject.should_not be_nil
  end
end"

def get_lib_template(klass_name)
  LIB_TEMPLATE.gsub(KLASS_NAME_DEFAULT, klass_name)
end

def get_spec_template(klass_name, file_name)
  result = SPEC_TEMPLATE.gsub(KLASS_NAME_DEFAULT, klass_name)
  result = result.gsub(FILE_NAME_DEFAULT, file_name)
end

def get_klass_name(file_name)
  klass_name = file_name.split('_').collect {|s| s.capitalize }.join
end

directory 'lib'
rule %r{lib\/.+\.rb} => ['lib'] do |file|
  File.open(file.name, "w+") do |f|
    base_name = File.basename(file.name, '.rb')
    klass_name = get_klass_name(base_name)
    f.write(get_lib_template(klass_name))
  end
end

directory 'spec'
rule %r{spec\/.+_spec\.rb} => ['spec'] do |file|
  File.open(file.name, "w+") do |f|
    base_name = File.basename(file.name, '_spec.rb')
    klass_name = get_klass_name(base_name)
    f.write(get_spec_template(klass_name, base_name))
  end
end

desc "Creates a sample lib/ and spec/"
task :create, [:klass_name] do |t, args|
  args.with_defaults(:klass_name => "kata_class")

  file_name = args.klass_name.downcase
  lib_file = File.join('lib', "#{file_name}.rb")
  spec_file = File.join('spec', "#{file_name}_spec.rb")

  Rake::Task[lib_file].invoke
  Rake::Task[spec_file].invoke
end

task :default => [:create]
