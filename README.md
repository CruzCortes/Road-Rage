globals [
  road-rager
  lanes 
]

turtles-own [
  speed
  top-speed
  target-lane
  tolerance
  patience
  road-rage-mode
]

to setup 
  clear-all
  set-default-shape turtles "pablo"
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
  ask patches with [ abs pxcor <= 5 ]
  [set pcolor grey - 2.5 + random-float 0.25
  ]
end

