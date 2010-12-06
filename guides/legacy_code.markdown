#Revisiting Legacy Code#

These are a list of things to keep in mind, check for and apply to legacy code when working with it. Keeping to this will help us to transform our legacy code into current working code over time. These are also points that all reviewers should be applying to incoming code before it hits the develop line. Sharing these changes back with the developer is vital to improving everyone's common working knowledge.

###Order Includes From Least to Most Local to the Source File###

###Liberal Standard Algorithm Usage###

###Use cstdint types instead of those in typedefs.h#

There is one gotcha here with int8/uint8, they should be replaced with char/unsigned char respectively.
