# recursive-region-merging

First we recursively label each pixel based on their gray-level intensity.
We begin with the top left corner and then progress till the bottom right corner.
We need to make sure that adjacent pixels which fall within a given range of gray-level intensities (20 in this case) are given the same label.

After this step the neighbors of pixels having the same label are calculated and stored in the same list.

The mean of gray-level intensity of all such neighbor groups is calculated.

Based on this mean value the neighbors are again merged to detect objects and boundaries.
