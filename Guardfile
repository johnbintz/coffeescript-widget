guard 'compass' do
  watch(%r{^sass/.*})
end

guard 'shell' do
  watch(%r{^src/.*}) do
    puts "Building..."
    system %{rake build}
    system %{open CoffeeScript.wdgt}
  end
end

