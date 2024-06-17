### S2: Geospatial indexing system
S2 is a square-shaped hierarchical geospatial indexing system created by Google. Tinder use S2 to recommend people in real time and shard the location database.  
S2 divides Earth’s surface into cells on a flat grid, giving each cell a unique identifier with a 64-bit integer. In other words, a small cell represents a small area of the earth. They store the users physically closer to each other in the same database shard. Thus reducing the need to query many shards to find nearby users.


### KISS (Keep it simple stupid)


### SOLID principles


### Conway's Law
Conway’s Law is an IT theory created by computer scientist/programmer Melvin Conway in 1967. Conway’s Law states that “Organizations, who design systems, are constrained to produce designs which are copies of the communication structures of these organizations.”
![Alt text](Images/conways-law.jpeg?raw=true "Title")  