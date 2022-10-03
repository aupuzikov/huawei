# классификация по полу датасета LibriTTS

модель везде использовалась
    
    Conv2d(1, 15, kernel_size=(3,3), stride=2, padding_mode='zeros'),
    MaxPool2d(kernel_size=(3,3), stride=2),
    LeakyReLU(),
    Conv2d(15, 45, kernel_size=(5,5), stride=2, padding_mode='zeros'),
    MaxPool2d(kernel_size=(5,5), stride=2),
    LeakyReLU(),
    Conv2d(45, 65, kernel_size=(5,5), stride=2, padding_mode='zeros'),
    MaxPool2d(kernel_size=(5,5), stride=2),
    LeakyReLU(),
    Flatten(),
    Linear(780, 1),
    Sigmoid()


| model | accuracy |
|---------|-----------|
| no_overlap+boxcar | 0.726 |
| overlap+boxcar | 0.732 |
| overlap+hahn |0.76 |
| overlap+hahn+log | 0..762 |
| overlap+hahn+melspec+log | 0.876 |
=======


| model      | accuracy |
| ----------- | ----------- |
| stft+no_overlap+boxcar      | 0.726       |
| stft+overlap+boxcar      | 0.732       |
| stft+overlap+hahn   | 0.763        |
| stft+overlap+hahn+log   | 0.774        |
| stft+overlap+hahn+melspec+log   | 0.876        |
