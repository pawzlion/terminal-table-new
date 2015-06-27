# terminal-table-new
A fixed version of tj's non-functional terminal-table library

I found that tj's terminal-table library would not function on any system
because it failed to include three key library files in the gemspec,
specifically table.rb, separator.rb, and style.rb

The new line 13 of the gemspec now looks like this:

  s.files = ["History.rdoc", "Manifest", "README.rdoc", "Rakefile",
  "Todo.rdoc", "examples/examples.rb", "lib/terminal-table.rb",
  "lib/terminal-table/cell.rb", "lib/terminal-table/import.rb",
  "lib/terminal-table/table.rb", "lib/terminal-table/table_helper.rb",
  "lib/terminal-table/version.rb", "lib/terminal-table/row.rb",
  "lib/terminal-table/separator.rb", "lib/terminal-table/style.rb",
  "spec/cell_spec.rb", "spec/import_spec.rb", "spec/spec_helper.rb",
  "spec/table_spec.rb", "tasks/docs.rake", "tasks/gemspec.rake",
  "tasks/spec.rake", "terminal-table.gemspec"]

This gem now compiles and works as it should.

To compile it, execute:

gem build terminal-table.gemspec

To install it, execute:

sudo gem install terminal-table-xxxx.gem

(Where xxxx is the version number of the gem produced in the build stage)
