# Glimy
## FDTD Simulator
  The electromagnetic field.. Interacts with our reality and the reason that we continue to live. We can live beter, if we know time evolution of electromagnetic field. 


<pre>
|----Continuum(object)----|
|                         |---__init__(dim,grid_size,ds)
|                         |---add(arg)
|                         |---add_energizer(arg)
|                         |---view_structure(bypass=True,*kwargs)
|                         |---view_field(*kwargs)
|                         |---export_for_renderer()
|                         |---load_from_renderer(E,H)
|                         |---export_E_field()
|
|
|
|---Render(field,n_time_steps)
|
|
|
|----DotSource(object)----|
|                         |---__init__(location,presence,amplitude,frequency,phase=0)
|                         |---__repr__()
|                         |---inf()
|                         
| 
| 
|----geo1D(module)--------|----Line(object)---------|
|                                                   |---__init__(A, B, layer, e=1, mu=1)
|                                                   |---__repr__()
|                                                   |---inf()
|                                                   |---t()
|                                                   |---isIn(point)
| 
| 
|                                                   
|----geo2D(module)--------|----Rectangle(object)----|
|                         |                         |---__init__(A,B,layer,e=1,mu=1)
|                         |                         |---__repr__()
|                         |                         |---inf()
|                         |                         |---t()
|                         |                         |---isIn(point)
|                         |
|                         |
|                         |----Circle(object)-------|
|                                                   |---__init__(A,r,layer,e=1,mu=1)
|                                                   |---__repr__()
|                                                   |---inf()
|                                                   |---t()
|                                                   |---isIn(point)
|
|
|
|----geo3D(module)--------|----RectPrism(object)----|
                          |                         |---__init__(A,B,layer=0,e=1,mu=1)
                          |                         |---__repr__()
                          |                         |---inf()
                          |                         |---t()
                          |                         |---isIn(point)
                          |
                          |
                          |----Sphere(object)-------|
                          |                         |---__init__(C,r,layer=0,e=1,mu=1)
                          |                         |---__repr__()
                          |                         |---inf()
                          |                         |---t()
                          |                         |---isIn(point)
                          |
                          |
                          |----Cylinder(object)-----|
                                                    |---__init__(C,r,h,layer=0,e=1,mu=1)
                                                    |---__repr__()
                                                    |---inf()
                                                    |---t()
                                                    |---isIn(point)
  </pre>
  
  # Documentation
  
  ## Continuum(dim,grid_size,ds)
   Creates electromagnetic field with given dimensions and grid size. Grid spacing is introduced with ds.
   - **dim** : Number of dimensions of the Continuum. It may take 1, 2 or 3.
   - **grid_size** : Deines grid cell count per axis. It may take a tuple orlist. It's lenghts must be the same as # of dimensions.
   - **ds** : Length of a edge of a grid cell.
     
     
  ## Render(field,n_time_steps)
   Executes FDTD calculations on a Continuum object.
   - **field** : It must take Continuum object. It s the field that evolved through time.
   - **n_time_steps** : It is number of time steps that field will evolve. Lenght of time steps is given by ds/c/(<span>&#8730;</span>dim) .
  
  
  ## DotSource(location,presence,amplitude,frequency,phase=0)
   Creates a point source on a given place on grid, through given time interval with given amplitude, frequency and phase.
  
  ## geo1D.Line(A, B, layer, e=1, mu=1)
  
  ## geo2D.Rectangle(A, B, layer, e=1, mu=1)
  
  ## geo2D.Circle(A,r,layer,e=1,mu=1)
  ## geo3D.(A, B, layer, e=1, mu=1)
  ## geo3D.Sphere(C,r,layer=0,e=1,mu=1)
  ## geo3D.Cylinder(C,r,h,layer=0,e=1,mu=1)
  
  
