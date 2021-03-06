# Cat Conditional DCGAN

This is based on pytorch DCGan enhanced to be conditional. 

### Instructions

```
	#untar the cat dataset with 4 classes of cats
	tar xvf hand_crafted_aug.tar.gz

	#if using gpu
	python gan_model.py --dataset=folder --dataroot=./dataset/hand_crafted_aug --nc=3 --cuda --ngpu=4 --niter=500 --cond

	#if using cpu
	python gan_model.py --dataset=folder --dataroot=./dataset/hand_crafted_aug --nc=3 --niter=50 --cond

	#if using cpu mnist
	python gan_model.py --dataset=mnist --dataroot=./mnist --nc=1 --niter=50 --cond

```

And to generate random images

```
	#for golden cats
	python gan_generate.py --netG=./netG_epoch_6.pth --num_classes=4 --nc=3 --the_class=1

	#for mnist
	python gan_generate.py --netG=./netG_epoch_6.pth --num_classes=10 --nc=1 --the_class=0
```

### Generated Cats

Black cats generated by conditional DCGAN. 

![Screenshot](results/final_samples_epoch_000.png)

Golden cats generated by conditional DCGAN. 

![Screenshot](results/final_samples_epoch_001.png)

Mixed cats generated by conditional DCGAN. 

![Screenshot](results/final_samples_epoch_002.png)

White cats generated by conditional DCGAN. 

![Screenshot](results/final_samples_epoch_003.png)