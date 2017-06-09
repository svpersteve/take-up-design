desc "Build the website from source"
task :build do
  puts "## Building website"
  status = system("middleman build --clean")
  puts status ? "OK" : "FAILED"
end

desc "Run the preview server at http://localhost:4567"
task :preview do
  system("middleman server")
end

desc "deploy to github pages"
task :deploy do
  p "## Deploying to Github Pages"
  cd "build" do
    system "touch CNAME"
    system "echo 'takeupdesign.com' >> CNAME"
    system "git add ."
    message = "Site updated at #{Time.now.utc}"
    p "## Commiting: #{message}"
    system "git commit -m \"#{message}\""
    p "## Pushing generated website"
    system "git push origin master -f"
    p "## Github Pages deploy complete"
  end
end

desc "build and deploy to github pages"
task :publish do
  Rake::Task["build"].invoke
  Rake::Task["deploy"].invoke
end
