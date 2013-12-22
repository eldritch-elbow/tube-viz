tube-viz
========

## Processing Steps

Downloaded CSV data from:
http://www.tfl.gov.uk/businessandpartners/syndication/16493.aspx

Detect all unique starting locations

	cat Nov09JnyExport.csv | awk -F ',' '{print $4}' > starts.txt

Same with ending locations, then uniqued both:

  cat ends.txt | sort | uniq > ends_uniq.txt

## References

Similar examples:

http://www.guardian.co.uk/news/datablog/interactive/2012/nov/01/london-underground-traffic-over-typical-day-tube-stations
