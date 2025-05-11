# Functions Documentation

## `rotmat2zyz`
Converts a rotation matrix into its corresponding ZYZ Euler angles.

**Inputs:**
- `R` - 3x3 rotation matrix
- `prev_theta` - (optional) previous value of theta to resolve ambiguity (default: $\pi/2$)

**Outputs:**
- `phi` - first ZYZ Euler angle in radians
- `theta` - second ZYZ Euler angle in radians
- `psi` - third ZYZ Euler angle in radians

**Author:** Daniyal Maroufi

## `rotmat2rollpitchyaw`
Converts a rotation matrix into its corresponding roll, pitch, and yaw angles.

**Inputs:**
- `R` - 3x3 rotation matrix
- `prev_theta` - (optional) previous value of theta to resolve ambiguity (default: 0)

**Outputs:**
- `phi` - roll angle in radians
- `theta` - pitch angle in radians
- `psi` - yaw angle in radians

**Author:** Daniyal Maroufi

## `rotmat2quaternion`
Converts a rotation matrix into its corresponding quaternion representation.

**Inputs:**
- `R` - 3x3 rotation matrix

**Outputs:**
- `q` - 4-element column vector representing the quaternion $[q_0; q_1; q_2; q_3]$

**Author:** Daniyal Maroufi

## `rotmat2axisangle`
Converts a rotation matrix into its corresponding axis-angle representation.

**Inputs:**
- `R` - 3x3 rotation matrix

**Outputs:**
- `axis` - 3-element column vector representing the axis of rotation
- `angle` - scalar value representing the angle of rotation in radians

**Author:** Daniyal Maroufi

## `quaternion2rotmat`
Converts the quaternion representation of a rotation in a 3D space into its corresponding rotation matrix.

**Inputs:**
- `scalar` - scalar value of quaternion or 4-element column vector quaternion
- `vector` - 3-element column vector of quaternion

**Outputs:**
- `rotmat` - 3x3 rotation matrix 

**Author:** Anas Yousaf

## `axisangle2rotmat`
Converts the axis-angle representation of a rotation in a 3D space into its corresponding rotation matrix.

**Inputs:**
- `axis` - 3-element column vector representing the axis of rotation
- `angle` - scalar radian representing the angle of rotation

**Outputs:**
- `rotmat` - 3x3 rotation matrix 

**Author:** Anas Yousaf

## `is_valid_rotation_matrix`
Checks if the input matrix is a valid rotation matrix.

**Inputs:**
- `R` - 3x3 matrix to be checked
- `check_identity` - (optional) boolean flag to check if the matrix is the identity matrix (default: true)

**Outputs:**
- `is_valid` - boolean indicating whether the input matrix is a valid rotation matrix

**Author:** Daniyal Maroufi

## `isequal_tol`
Checks if two matrices are equal within a specified tolerance.

**Inputs:**
- `A` - first matrix
- `B` - second matrix
- `tol` - (optional) tolerance value (default: $1 \times 10^{-6}$)

**Outputs:**
- `isEqual` - boolean indicating whether the matrices are equal within the specified tolerance

**Author:** Daniyal Maroufi

## `transfmat2screw`
Converts the transformation matrix of a transformation in a 3D space into its corresponding screw axis representation.

**Inputs:**
- `transfmat` - 4x4 transformation matrix 

**Outputs:**
- `point` - 3-element vector describing the point on the rotation axis
- `axis` - 3-element vector describing the rotation axis
- `pitch` - scalar element describing the pitch of the screw axis
- `angle` - scalar angle in radians describing the distance along the screw

**Author:** Anas Yousaf

## `screw2transfmat`
Converts the screw axis representation of a transformation in a 3D space into its corresponding transformation matrix.

**Inputs:**
- `point` - 3-element vector describing the point on the rotation axis
- `axis` - 3-element vector describing the rotation axis
- `pitch` - scalar element describing the pitch of the screw axis
- `angle` - scalar angle in radians describing the distance along the screw

**Outputs:**
- `transfmat` - 4x4 transformation matrix 

**Author:** Anas Yousaf

## `plotTransformAxes`
Plots the axes of a frame defined by the input transformation matrix.

**Inputs:**
- `transfmat` - 4x4 transformation matrix

**Outputs:**
- `axes` - column vector for each axis that is plotted

**Author:** Anas Yousaf

## `plotScrewAxis`
Plots the screw axis defined by the input in a 3D space.

**Inputs:**
- `point` - 3-element vector describing the point on the rotation axis
- `axis` - 3-element vector describing the rotation axis
- `pitch` - scalar element describing the pitch of the screw axis

**Outputs:**
- `axes` - column vector for each axis that is plotted

**Author:** Anas Yousaf

## `inputTransfmatScrew`
Takes in an initial screw axis, distance, and transformation matrix and finds the final transformation configuration. Plots the initial, intermediate, and final transformation configurations. Calculates and returns the screw axis and distance to return the final configuration to the origin.

**Inputs:**
- `T_initial` - 4x4 transformation matrix of original configuration
- `p` - 3-element vector describing the initial point on the rotation axis
- `s_hat` - 3-element vector describing the initial rotation axis
- `h` - scalar element describing the pitch of the initial screw axis
- `theta` - scalar angle in radians describing the initial distance 

**Outputs:**
- `T_final` - 4x4 transformation matrix of final configuration
- `T_intermediate` - cell array containing initial, intermediate, and final transformation matrices
- `point` - 3-element vector describing the point on the rotation axis
- `s_axis` - 3-element vector describing the rotation axis
- `pitch` - scalar element describing the pitch of the screw axis
- `angle` - scalar angle in radians describing the distance along the screw

**Author:** Anas Yousaf

## `is_valid_transform_matrix`
Determines if an input matrix is a valid 4x4 homogeneous transformation.

**Inputs:**
- `transfmat` - 4x4 transformation matrix

**Outputs:**
- `result` - returns true if valid matrix, false otherwise

**Author:** Anas Yousaf
