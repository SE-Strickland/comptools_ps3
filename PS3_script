 #!/usr/bin/env python3

### Comp Tools PS 3

## Question 1:

#Open the file
data = open('/blue/bsc4452/share/Class_Files/data/CO-OPS_8727520_wl.csv')

#skip the headerline
next(data)

#initialize variables 
max_water_level = 0

for line in data:
    columns = line.strip().split(',')
    date = columns[0]
    time = columns[1]
    water_level = float(columns[3].strip('"'))
    
    if max_water_level < water_level:
        max_water_level = water_level
        max_water_level_date = date
        max_water_level_time = time   
print(f"The max water level is: {max_water_level} ft. observed on {max_water_level_date} at {max_water_level_time}")

## Question 2:

#Open the file
data = open('/blue/bsc4452/share/Class_Files/data/CO-OPS_8727520_wl.csv')

#skip the headerline
next(data)

#initialize variables 
max_water_level = 0

for line in data:
    columns = line.strip().split(',')
    date = columns[0]
    time = columns[1]
    water_level = float(columns[3].strip('"'))
    
    if max_water_level < water_level:
        max_water_level = water_level
        max_water_level_date = date
        max_water_level_time = time   
print(f"The max water level is: {max_water_level} ft. observed on {max_water_level_date} at {max_water_level_time}")

## Question 3:

data = open('/blue/bsc4452/share/Class_Files/data/CO-OPS_8727520_wl.csv')

#skip the headerline
next(data)

#initialize variables 
previous_water_level = "None"
greatest_water_level_difference = 0

for line in data:
    columns = line.strip().split(',')
    date = columns[0]
    time = columns[1]
    water_level = float(columns[3].strip('"'))
    
    if not previous_water_level == "None":
        new_water_level_difference = water_level - previous_water_level
        
        if new_water_level_difference > greatest_water_level_difference:
            greatest_water_level_difference = new_water_level_difference
            wl_dif_date = date
            wl_dif_time = time
        previous_water_level = water_level
    
    else:
        previous_water_level = water_level
    
print(f"The fastest rise in water-level over the 6-minute measuring period was {greatest_water_level_difference:.2f} ft. on {wl_dif_date} at {wl_dif_time}.")
    
 ## Question 4: 

data = open('/blue/bsc4452/share/Class_Files/data/CO-OPS_8727520_wl.csv') #Can input path to real-time file here instead

#skip the headerline
next(data)

# Initialize
current_water_change = 0
current_water_level = 0
previous_water_level = 0

for line in data: 
    columns = line.strip().split(',')
    date = columns[0]
    time = columns[1]
    water_level = float(columns[3].strip('"'))
    
    if water_level == "": # Warning for no water_level data
        print(f"WARNING - No reading recived: There is no water level reading recorded for {data} at {time}.")
    
    if water_level > 5.0: #Warning for high water level
        print(f"WARNING - Water level greater than 5 ft: As of {date} at {time}, current water level is {water_level} ft.") 
    
    #Warning for large rise in water level
    change_in_water_level = water_level - previous_water_level
    
    if change_in_water_level > 0.25 and previous_water_level != "None":
        print(f"WARNING - Water level rise greater than 0.25 ft: As of {date} at {time}, the water level has risen by {change_in_water_level} ft.") 
    
    #Preparing to repeat the loop
    previous_water_level = water_level

    #End of for loop
