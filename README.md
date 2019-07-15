# gnuplot-dstat

Generate gnuplot PNG graphics from a dstat CSV file.
This is quite dirty but efficient so far.
I've been looking around for such utility, found a lot, but not really what I wanted.

To use it, first get a dstat CSV file. For example, with the command:
```
dstat -t -a --socket -p -C 0,1,2,3,total --aio --top-cpu --top-mem --output dstat.csv --noupdate --nocolor 5 &>/dev/null
```

Then, plot graphics with the command:
```
gnuplot-dstat -i dstat.csv -o /tmp/report
```

Results will be stored in /tmp/report folder.
![Network graph example](https://raw.githubusercontent.com/gmaquinay/gnuplot-dstat/master/examples/pc2_net_total.png)
