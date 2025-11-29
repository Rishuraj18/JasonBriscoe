<script>
// @ts-nocheck

    import {fade,fly} from 'svelte/transition';
   
     let isClicked = $state(false);
     const handleClick = () => {
    isClicked = !isClicked; 
    console.log(isClicked);
};
import { slide } from 'svelte/transition';
import { onMount } from 'svelte';
		let visible = $state(false);

	onMount(() => {
		visible = true;  
	});
   


</script>
<main>
    <div class="overflow-x-hidden pl-8 pr-6 lg:px-2 lg:overflow-x-hidden lg:p-8 lg:pr-6">
{#if visible}
<div in:fly={{ y: 100, duration: 2000 }} out:fade>

<div class="overflow-x-hidden pl-8 pr-6 lg:px-2 lg:overflow-x-hidden lg:p-8 lg:pr-6">

<div class=" flex flex-col items-center justify-center m-8 md:p-10">
    <span class="text-2xl font-bold md:font-medium">Jason Briscoe</span>
</div>
</div>
</div>
{/if}
{#if visible}
<div in:fly={{ x:-200, duration: 2000 }} out:fade>
    <div class="w-auto  text-3xl font-bold mt-20  lg:w-7/10 lg:ml-40 lg:text-8xl md:text-6xl m-8">
        <p class=" ">Design Pattern for early stage tech and scale ups.</p>
    </div>
</div>
{/if}
{#if visible}
<div in:fly={{ x:200, duration: 2000 }} out:fade>
    <div class=" ml-10 mt-20 text-xl font-light lg:ml-100 lg:mr-20 md:ml-70 md:mr-30 md:text-2xl ">
        <p class="">
             I've spent a couple of decades creating brands and digital products -- acting as a VP of desin,co-founder and advisor. Based in London,Tornto and NYC</p>
        <p class=" mt-10">My Studio <a href="https://www.google.com"target="_blank"class="underline hover:no-underline">The Workshop</a> partners with founders and VC to brand, build and bring product ideas to life.</p>
        <div class="my-8 flex gap-4">
            <a href="mail-to" class="underline hover:no-underline " >E-mail me</a>
            <a href="#Call" class="underline hover:no-underline ">Schedule a discovery call</a>
        </div>
    </div>

</div>
{/if}
 

    <div class="w-full bg-cover bg-center mt-20  transform transition-all duration-1000 hover:scale-110 ">
        <img  src="https://jasonbriscoe.com/jb.jpg" alt="Jason" class="rounded-4xl h-[400px] lg:w-8/10 lg:ml-35 lg:rounded-3xl lg:h-full md:p-4 md:h-[500px]" >
    </div>


    <div class="my-20 text-4xl mx-6 font-bold lg:ml-130 lg:text-9xl md:ml-60 md:mt-50 md:text-8xl">
            <span>Concept.</span>
            <span >Brand. Build.</span>
            <span >Launch. Exit.</span>
    </div>
  

    <div class="w-full md:p-5 ">
         <img class="rounded-4xl h-[250px] w-full lg:h-[600px] lg:w-8/10 lg:ml-30 md:rounded-4xl md:h-[400px]" src="https://media.giphy.com/media/l0Ex7VSPBXHKW9WOA/giphy.gif?cid=790b7611fajnw8maidutjt5j5imcbxmmcc31jcclmpompobl&ep=v1_gifs_search&rid=giphy.gif&ct=g" alt="Nothing">
    </div>


    <div class="w-auto ml-16 md:ml-60 md:mr-30 md:text-2xl">
        <p class="my-10 lg:ml-90 lg:text-3xl lg:mr-20 ">
            I help companies make strategic foundational decisions and leverage their position in the market — providing long-term support, often through a blend of cash and equity.</p>
        <p class=" lg:ml-90 lg:text-3xl lg:mr-20">In recent years, I've helped build multiple businesses leading to over $55M in capital investment.</p>
    </div>


    <div class=" w-full mt-40 ">
         <h1 class= "text-4xl font-bold lg:text-9xl lg:ml-30 lg:font-bold md:mx-20 md:text-6xl">
            Here's what you can expect from me...</h1>
    </div>

    <div class="button1 w-full flex">
        <button class="my-10 mx-auto bg-pink-400 rounded-lg w-48 h-16"onclick={handleClick}>Click Me</button>
    </div>
    

    {#if isClicked}
	<p transition:fade></p>;
	
	
    <div class="lg:flex lg:flex-wrap lg:gap-15 lg:mt-30 md:flex md:flex-wrap md:mx-5 md:gap-14 md:mt-30"
         transition:slide|global >
        <div class="bg-emerald-500 my-8 rounded-xl  transition-transform duration-1500 h-110 hover:scale-115 lg:w-3/10 lg:ml-30 lg:my-0 md:w-3/10 md:h-[300px] md:my-0">
           <p class="p-8 text-xl font-bold">Value</p>
           <p class="mx-5 text-2xl font-bold">Experience, big energy and fresh thinking.</p>
        </div>
        <div class="bg-yellow-200 rounded-2xl my-8  transition-transform duration-1500 h-110 hover:scale-115 lg:w-5/10 lg:my-0 md:w-5/10 md:h-[300px] md:my-0">
            <p class="p-8 text-xl font-bold">Jordon Nott,Founder</p>
            <p class="mx-5 text-2xl font-bold">"It’s very rare in life when you meet someone that is so decisively exceptional at what they do."</p>
        </div>
        <div class=" bg-[rgba(255,134,90,0.91)] rounded-2xl my-8 transition-transform duration-1500 h-110 hover:scale-115 lg:w-4/10 lg:ml-30 lg:my-0 md:w-4/10 md:h-[300px] md:my-0" >
            <p class="p-8 text-xl font-bold">Insights</p>
            <p class="mx-5 text-2xl font-bold"> Bridge the gap between creative and commercial objectives — speaking both languages.</p>
        </div>
        <div class=" bg-cyan-300 rounded-2xl my-8 transition-transform  duration-1500 h-110 hover:scale-115 lg:w-4/10 lg:my-0 md:w-4/10 md:h-[300px] md:my-0 ">
            <p class="p-8 text-xl font-bold">Peter Hwang, Founder</p>
              <h3 class="mx-5 text-2xl font-bold">"From a creative perspective, I’ve never worked with a more talented individual."</h3>
        </div>
        <div class=" bg-[rgb(40,101,142)] rounded-2xl my-8 transition-transform duration-1000 h-110 hover:scale-115 lg:w-5/10 lg:ml-30 lg:my-0 md:w-5/10 md:h-[300px] md:my-0">
            <p class="p-8 text-xl font-bold">Growth</p>
            <h3 class="mx-5 text-2xl font-bold">The foundations to scale — from world-class design and advisory to building your future team.</h3>
        </div>
        <div class="bg-[rgb(112,77,152)] rounded-2xl my-8 transition-transform duration-1000 h-110 hover:scale-110 lg:w-3/10 lg:my-0 md:w-3/10 md:h-[300px] md:my-0">
            <p class="p-8 text-xl font-bold">Fun</p>
            <h3 class="mx-5 text-2xl font-bold">Teach teams to move at velocity and have a hell of a lot of fun doing it.</h3>
        </div>
    </div>

{/if}
    <div class="ml-15 my-8 lg:mt-30 lg:ml-140 lg:mr-40 lg:text-xl md:mt-40 md:ml-60 md:mr-35">
         <p class="my-6">
            Culturally, I fit high-energy and fun management teams.</p>
        <p class="my-6">
            I compete in Hyrox races around the world, care deeply about being a present father and husband, and maintain a healthy balance between work, life and play.</p>
        <p class="my-6">
            Feel free to <a href="mailto:rrishuraj12345678@gmail.com">email me</a>, <a href="tel:+1234567">schedule a call</a> or connect on <a href="#linkedin">LinkedIn</a>.</p>
        <p class="my-6">
            Let’s have some fun!</p>
    </div>


    <div class="mr-30 lg:ml-120 mb-10 md:ml-40 ">
        <img class="lg:h-[200px] md:h-[200px]"src="msd.png" alt="Sinature">
    </div>


    <div class=" mt-20 flex flex-wrap-reverse items-center ml-20 lg:justify-between lg:mt-0 md:justify-start md:my-8 md:mx-0">
        <p class=" my-4 lg:my-0  md:my-0  ">
        &copy;Jason Briscoe &#128075</p>
        <ul class=" flex gap-6 mr-30 md:ml-100 md:mr-0 ">
            <li><a href="#Linkedin"class="underline hover:no-underline">Linkedin</a></li>
            <li><a href="#Cv"class="underline hover:no-underline">ReadCv</a></li>
            <li><a href="#X"class="underline hover:no-underline">X</a></li>
     </ul>
     
    </div>
    </div>
</main>

