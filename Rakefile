require 'rake'

desc 'Build configuration files'
task :build do
  Dir.chdir('configs') do
    Dir.glob('*') do |f|
      if File.file?(f)
        `arethusa merge #{f} -b . > ../dist/#{f}`
        puts "Created #{f}"
      end
    end
  end
end
