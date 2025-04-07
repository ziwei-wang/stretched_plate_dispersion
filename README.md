# Stretched Plate Dispersion

## Abaqus Model
file name: `main.cae`
### Adjust the thickness of the model.

Change the thickness of the plate. 

<img width="1665" alt="image" src="https://github.com/user-attachments/assets/59070ca7-d97d-4808-ad84-60cb90605ad1" />

### Change material model

Current model is a hyperelastic-viscoelastic model. It can be changed here. \
<img width="726" alt="image" src="https://github.com/user-attachments/assets/dacf50b8-e2d6-412b-ace2-f2eca3720783" />


### Change static stretch ratio

Just change the displacement applied to the plate in x direction.

<img width="1630" alt="image" src="https://github.com/user-attachments/assets/d217ea14-62cd-4978-a805-59f90f568eb6" />

### Set up wave propagation and frequency range

Vibration source is the short edge, with harmonic displacement in y direction.

<img width="886" alt="image" src="https://github.com/user-attachments/assets/9603e601-4edd-4796-b813-e00647aeb128" />


Currently, the model calcualtes steady state solution from 2000 Hz to 5000 Hz, with 2 frequency points. 

<img width="941" alt="image" src="https://github.com/user-attachments/assets/0ef3cebd-bfc0-47f9-b5f9-074e01d67194" />

### Submit Abaqus job
<img width="264" alt="image" src="https://github.com/user-attachments/assets/08f99abf-05ee-4471-aa4e-005f798979c0" />

## Post Processing
file name `Post/post.py`

It extracts displacement field along the `TOP_EDGE` for each frequency.

### Run post processing
In Abaqus CAE, click `File/Run Script`. 

Select `Post/post.py`.

The profile will be extracted as `Profile_Job-1.csv`.

## Calculate wave speeds and decay factors

Open `Post/speed.ipynb` with Jupyter notebook.

Run the code and make sure to import the profile extracted with the `post.py`

This will generate wave speeds and decay factors for all frequencies contained in the profile file.







