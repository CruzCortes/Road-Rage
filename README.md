globals [
  road-rager
  lanes
]

turtles-own [
  speed       
  top-speed     
  target-lane  
  patience      
]

to setup
  clear-all
  set-default-shape turtles "pablo"
  create-turtles 1
  ask turtles
  [
    set shape "pablo"
    set size 4
  ]
  draw-ground
  draw-road
  reset-ticks
end

to draw-ground
  ask patches [
  set pcolor 56 - random-float 0.2
  ]
end


to draw-road
  ask patches with [ abs pxcor <= 10 ]
  [set pcolor grey - 2.5 + random-float 0.25
  ]
  ask patches with [ abs pxcor <= 9 ]
  [set pcolor grey
  ]
end

to go
  ask turtles 
  [
    forward 1
  ]
  tick
end

