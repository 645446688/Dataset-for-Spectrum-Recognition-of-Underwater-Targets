# DemonData_1chn_max.mat
This part is a single-channel dataset for network training, and the samples contained in it are single-channel.
# DemonData_6chn.mat
This part is a 6-channel dataset for network training, and the samples contained in it are 6-channel.
# DemonData_Dop_1chn_max.mat/DemonData_Dop_6chn.mat
These two datasets contain samples with different degrees of Doppler frequency shift, which are used to evaluate the Doppler effect.
# DemonData_LowSNR_1chn_max.mat/DemonData_LowSNR_6chn.mat
These two datasets contain samples with different degrees of signal-to-noise ratio, which are used to evaluate the signal-to-noise ratio effect.
# DemonData_LostInterference_1chn_max.mat/DemonData_LostInterference_6chn.mat
These two datasets contain samples with different kinds of interferences, which are used to evaluate the interferences effect.

# Instructions
When you need to import a data set, you can use the following methods:
# Import training dataset
path = r'pathname'
data = h5py.File(path)
X_data = np.transpose(data['X_data'])
Y_data = np.transpose(data['Y_data'])
del data
print('data has been imported!')

# Import evaluate dataset
path_t =r'pathname'
data_t = h5py.File(path_t)
CLASS_NUM = data_t['classnum'][0][0]
SAMPLE_NUM = data_t['samplenum'][0][0]
X_data = np.transpose(data_t['X_data'])
Y_data = np.transpose(data_t['Y_data'])
print(X_data.shape)
print(Y_data.shape)
del data_t
print('data has been imported!')