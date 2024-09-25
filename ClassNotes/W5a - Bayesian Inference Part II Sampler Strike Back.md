# Outline 
- Samplers
- things that could go wrong with samplers 
- what sampler should do 
- eyeballing your sampler 
- diag
- sampling cat variables
# Sampler Review 
- basic idea
	- find where in the parameter space the posterior is 
	- sample from that region of parameter space 
- if goes well your set of samples can be used to characterize your posterior distribution 

**important notes**: you can mix and match sampling steps 
# Types of Samplers
- Gibbs sampler
	- iterate through sampling form proper conditional distributions 
	- require that you have proper conditional distribution
	- always use Gibbs if possible it's powerful and has guaranteed performance 
- Random walk metropolis 
	- when you don't have nice conditional distribution (improper)
	- requires you specify a proposal distribution for each parameter
		- important choice impacts convergence and performance
	- sampler walks through parameter space trying to find the posterior 
	- performance depends on 
		- tuning, prior, structure
- Random Walk Metropolis Hasting 
- Hamiltonian MC 
	- better version of metropolis hastings 
	- use gradient information 
	- not appropriate for use on categorical variables 
		- if you have no gradient information you can't use Hamiltonian MC
- NUT sampler 
	- fixes issues in Hamiltonian MC 
# What Should Samplers  Do? 
> if everything is right sampler should converge to the posterior and stay there forever 

well constructed sampers are ergodic 
- they cover the whole space
- which means they tend to find the posterior 

**You can have an appropriate model and still have sampler issues**
# What goes wrong with samplers? 
> samplers are highly sensitive to the topology of the parameter space

if the space is nice the sampler or ergodic 
**Finish later** 
# Sampler Pathologies - An informal guide
- add slides 
# Geweke's Z-score Diag
- convergence - when the sampler has settled into the posterior and will remain for the rest of the time
- in a converged chain, the e
