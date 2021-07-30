<script context="module">
	export const prerender = true;
</script>
<script>
	import States from '$lib/States.svelte'
</script>
<form data-netlify="true"  method="post" name="customer">
  <input type="hidden" name="form-name" value="customer" />
  <section class="header relative pt-16 items-center flex  max-h-860-px">
    <div class="container mx-auto items-center flex flex-wrap">
      <div class="w-full">
        <div class="pt-32 sm:pt-0">
          <h2 class="font-semibold text-4xl text-blueGray-600">
            Hybrid Heros are mobile hybrid mechanics
          </h2>
          <h3 class="text-green-500">who come to you!</h3>
  
          <h3 class="italic text-gray-800">Find a hybrid mechanic near your location</h3>
  <States/>
          <p class="mt-3">
            Let us know where and we will let you know when we service that area.
          </p>
            
  
          <p class="mt-4 text-lg leading-relaxed text-blueGray-500">
            Our mechanics are trained and vetted. Work is guaranteed.
            <!-- <a
                href="https://tailwindcss.com/?ref=creativetim"
                class="text-blueGray-600"
                target="_blank"
              >
                Tailwind CSS.
              </a> -->
            Get a free quote over the phone, or, even better, have a mechanic come to you to evaluate your
            hybrid.
          </p>
          <!-- <div class="mt-12">
              <a
                href="https://www.creative-tim.com/learning-lab/tailwind/svelte/overview/notus?ref=ns-index"
                target="_blank"
                class="get-started ml-1 text-white font-bold px-6 py-4 rounded outline-none focus:outline-none mr-1 mb-1 bg-red-400 active:bg-red-500 uppercase text-sm shadow hover:shadow-lg ease-linear transition-all duration-150"
              >
                Get a mechanic
              </a>
              <a
                href="https://github.com/creativetimofficial/notus-svelte?ref=ns-index"
                class="github-star ml-1 text-white font-bold px-6 py-4 rounded outline-none focus:outline-none mr-1 mb-1 bg-blue-400 active:bg-blue-600 uppercase text-sm shadow hover:shadow-lg ease-linear transition-all duration-150"
                target="_blank"
              >
                Get a quote
              </a>
            </div> -->
        </div>
      </div>
    </div>
  </section>
  <input type="text" name="zipcode" placeholder="Zipcode">
  <input type="text" name="name" placeholder="Your name">
  <input type="submit" value="Send" >
</form>

