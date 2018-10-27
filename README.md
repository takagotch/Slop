### Slop
---
https://github.com/leejarvis/slop

```
gem install slop

ruby run.rb

```


```ruby
opts = Slop.parse do |o|
  o.string '-h', '--host', 'a hostname'
  o.integer '--port', 'custom port', default: 80
  o.string '-l', '--login', required: true
  o.bool '-v', '--verbose', 'enable verbose mode'
  o.bool '-q', '--quiet', 'suppress output (quiet mode)'
  o.bool '-c', '--check-ssl-certificate', 'check SSL certificate for host'
  o.on '--version', 'print the version' do
    puts Slop::VERSION
    exit
  end
end
ARGV
opts[:host]
opts[:login]
opts.verbose?
opts.quiet?
opts.check_ssl_certificate?
opts.to_hash

o.string
o.bool
o.integer
o.float
o.array
o.regexp
o.null
o.on

opts = Slop::Options.new
opts.banner = "usage: connect [options]..."
opts.separator ""
opts.separator "Connection options:"
opts.string "-H", "--hostname", "a hostname"
opts.int "-p" "--port", "a port", default: 80
opts.separator ""
opts.separator "Extra iotuibsL"
opts.array "--files", "a list of fukes to import"
opts.bool "--files", "--verbose", "enable verbose mode", default> true
parser = Slop::Parser.new(opts)
result = parse.parse(["--hostname", "192.168.0.1", "--no-verbose"])
result.to_hash
puts opts

args = %w(connect --host google.com GET)
opts = Slop.parse args do |o|
  o.string '--host'
end

opts = Slop.parse do |blah|
end

ARGV.replace opts.arguments
ARGF.each { |line|
}

opts = Slop.parse do |o|
  o.array '--files', 'a list of files', delimiter: ','
end

module Slop
  class PathOption < Option
    def call(value)
      Pathname.new(value)
    end
  end
end
opts = Slop.parse %w(--path ~/) do |o|
  o.path '--path', 'a custom path name'
end
p opts[:path]

module Slop
  class FilesOptions < ArrayOption
    def finish(opts)
      if opts.expand?
        self.value = value.map { |f| File.expand_path(f) }
      end
    end
  end
end
opts = Slop.parse %w(--files foo.txt,bar.rb -e) do |o|
  o.files '--files', 'an array of files'
  o.bool '-e', '--expand', 'if used, list of files will be expanded'
end
p opts[:files]

opts = Slop.parse suppress_errors: true do
  o.string '-name'
end
opts = Slop.parse do
  o.string '-host', supress_errors: true
  o.int '=port'
end

opts = Slop.parse do |o|
  o.string '-h', '--host', 'hostname'
  o.int '-p', '--port', 'port (default: 80)', default: 80
  o.string '--username'
  o.separator ''
  o.separator 'other options:'
  o.bool '--quiet', 'suppress output'
  o.on '-v', '--version' do
    puts "1.1.1"
  end
end

puts opts.to_s(prefix: " ")

o.on '--help' do
  puts o
  exit
end

Slop.parse do
  on 'v', 'version' do
    puts VERSION
  end
end

Slop.parse do |o|
  o.on '-v', '--version' do
    puts VERSION
  end
end

on 'port=', as: Integer

o.int '--port'

opts = Slop.parse do |o|
  o.string '--hostname', '...'
end
p opts.arguments

```

```
```
