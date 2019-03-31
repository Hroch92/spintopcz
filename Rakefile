require "rake/contrib/ftptools"

task :default do    
    sh("bundle exec jekyll build")
    Dir.chdir('_site') do
    Rake::FtpUploader.connect('/www/subdom/jekyll/', ENV['FTP_HOST'], ENV['FTP_USER'], ENV['FTP_PASS']) do |ftp|
        ftp.verbose = true
        ftp.upload_files("./**/*")
      end
    end

end
