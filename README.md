# pcmrg
PCM audio replay gain computer

The program takes three arguments: the name of the PCM file, the audio frequency
('A' for 44.1kHz, 'B' for 48kHz, 'C' for 22.05kHz) and the number of channels
('1' for one, '2' for two).

The PCM sample is 16bit, signed integer.

It outputs an integral number, V, from which the replay gain may be computed as:

    'pow(10, (64.82 - V / 100) / 20)'
