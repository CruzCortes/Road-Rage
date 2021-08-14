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
  draw-road          
  reset-ticks
end

to draw-road
  ask patches [
    ; the road is surrounded by green grass of varying shades
    set pcolor 56 - random-float 0.2
  ]
end

