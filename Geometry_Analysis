import numpy
import os
def calculate_distance(coords1, coords2):
    """"
    This function has two arguments, the coordinates of two atoms. It returns the distance between two atoms.
    """
    x_distance=coords1[0]-coords2[0]
    y_distance=coords1[1]-coords2[1]
    z_distance=coords1[2]-coords2[2]
    distance_12=numpy.sqrt(x_distance**2+y_distance**2+z_distance**2)
    return distance_12
    def bond_check(distance):
    """
    Checks a distance to see if it;s a bond.
    """
    if distance >0 and distance<1.5:
        return True
    else:
        return False
        xyz_file=numpy.genfromtxt(fname=file_location, dtype='unicode', skip_header=2)
print(xyz_file)
symbols = xyz_file[:,0]
print(symbols)
coordinates=xyz_file[:,1:]
print(coordinates)
coordinates = coordinates.astype(numpy.float)
print(coordinates)
num_atoms=len(symbols)
for num1 in range(0, num_atoms):
    for num2 in range(0,num_atoms):
        if num1>num2:
            distance_12=calculate_distance(coordinates[num1], coordinates[num2])
            if bond_check(distance_12) is True:
                print(F'{symbols[num1]} to {symbols[num2]}:{distance_12:.3f}')
