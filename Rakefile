require 'rake'

desc 'Build configuration files'
task :build do
  Dir.chdir('pre_merge') do
    Dir.glob('*') do |f|
      if File.file?(f)
        `arethusa merge #{f} -b . > ../#{f}`
        puts "Created #{f}"
      end
    end
  end
end
