task :default do
  sh "ruby shp2ndjson.rb"
  sh "../tippecanoe/tippecanoe -f -o land.mbtiles --read-parallel --layer=land --maximum-zoom=8 land.ndjson"
  sh "ruby fan-out.rb"
end
