#
# GeoRuby Guardfile
#
ignore(/\/.#.+/)

guard :rubocop, all_on_start: false, cli: ['--format', 'emacs'] do
  watch(/^lib\/(.+)\.rb$/)
end

guard :rspec, cmd: 'bundle exec rspec' do
  watch(/^spec\/.+_spec\.rb$/)
  watch(/^lib\/(.+)\.rb$/)     { |m| "spec/#{m[1]}_spec.rb" }
  watch('spec/spec_helper.rb')  { 'spec' }
end
