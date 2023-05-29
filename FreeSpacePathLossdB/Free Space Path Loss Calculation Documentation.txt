function L = FreeSpacePathLossdB(d, f)
% FreeSpacePathLossdB calculates the free space path loss in decibels (dB)
% based on the distance and frequency.
%
% Inputs:
%   d: Distance between the transmitter and receiver (in meters)
%   f: Frequency of the signal (in Hertz)
%
% Output:
%   L: Free space path loss in decibels (dB)
%
% Example:
%   d = 10000;    % 10,000 meters
%   f = 900;      % 900 Hz
%   L = FreeSpacePathLossdB(d, f);
%
% Author: Marios Iosifidis
% Created: 29.5.2022
% Last modified: 29.5.2022

% Speed of light in meters per second
c = 3e8;

% Calculate the numerator and denominator for the path loss formula
numerator = 4 * pi * d;
denominator = c / f;

% Calculate the path loss in decibels (dB)
L = 20 * log10(numerator / denominator);

end
