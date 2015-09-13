#Tourmaline
![Tourmaline logo](https://raw.githubusercontent.com/demonh3x/tourmaline/master/img/logo200.jpg)

A gem to pipe ruby code in the command line

### Setup
* Clone this repo.
* Make sure the `rb` script has execution permissions by running `chmod +x rb` if necessary.
* Make sure the `rb` script is accessible in one of the execution paths in your `$PATH`. More information can be found [here](http://stackoverflow.com/questions/1234424/add-a-single-bash-command).

### Examples
`ping www.google.com | rb 'doing{STDIN.gets}.select{|l| l.include? "time="}.each{|l| puts l.split("time=")[1]}'`

`echo -e '1\n5\n3\n7\n' | rb 'puts lines.to_i.take(3).inject(0){|acc,num| acc + num}'`

`rb 'lines.upcase.take_while{|l| !l.include?("QUIT")}.puts.each'`

`rb 'doing{rand(1..6)}.puts.each'`
