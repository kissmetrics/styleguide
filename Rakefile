require 'rake'

SOURCE = "."
CONFIG = {
  'posts' => File.join(SOURCE, "_posts"),
}

desc "Create new stylesheet skeleton"
task :guide do
  abort("rake aborted: '#{CONFIG['posts']}' directory not found.") unless FileTest.directory?(CONFIG['posts'])

  title = ENV["title"] || "styleguide"
  slug = title.downcase.strip.gsub(' ', '-').gsub(/[^\w-]/, '')
  filename = File.join(CONFIG['posts'], "#{Time.now.strftime('%Y-%m-%d')}-#{slug}.md")
  puts "Creating new styleguide: #{filename}"

  default_headings = %w{coding-style documentation syntax naming classes exceptions collections strings regular-expressions}

  open(filename, 'w') do |post|
		post.puts "---"
		post.puts "layout: styleguide"
		post.puts "title: \"#{title.gsub(/-/,' ')}\""
		post.puts "---"
		post.puts ""
		post.puts "## Table of Contents"
		default_headings.each do | heading |
			post.puts "* [#{heading.capitalize}](##{heading})"
		end
		post.puts ""
		default_headings.each do | heading |
			post.puts "## <a id='#{heading}'></a>#{heading.capitalize}"
			post.puts "* Something they should do" 
			post.puts "* Something else they should do"
			post.puts ""
			post.puts "```"
			post.puts "# Bad"
			post.puts "x = code"
			post.puts "code should do something"
			post.puts ""
			post.puts "# Good"
			post.puts "x = code"
			post.puts "code should show something"
			post.puts "```"
			post.puts ""
		end
  end
end