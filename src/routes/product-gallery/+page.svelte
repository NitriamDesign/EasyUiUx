<script>
    const products = [
        { id: 1, name: 'Wireless Headphones', price: 99.99, category: 'Electronics', image: '/products/headset.webp', description: 'Sleek wireless headphones ' },
        { id: 2, name: 'Gaming Mouse', price: 49.99, category: 'Electronics', image: '/products/gaming-mouse.webp', description: 'Ergonomic gaming mouse with RGB lighting and programmable buttons.' },
        { id: 3, name: 'Coffee Maker', price: 79.99, category: 'Appliances', image: '/products/coffee-maker.webp', description: 'Compact coffee maker with a modern design and digital display.' },
        { id: 4, name: 'Yoga Mat', price: 29.99, category: 'Fitness', image: '/products/yoga-mat.webp', description: 'Purple yoga mat with a textured surface for better grip and comfort.' },
        { id: 5, name: 'Running Shoes', price: 119.99, category: 'Fitness', image: '/products/running-shoes.webp', description: 'Breathable running shoes with cushioned soles and stylish design.' },
        { id: 6, name: 'Desk Lamp', price: 39.99, category: 'Home Office', image: '/products/lamp.webp', description: 'Minimalist desk lamp with adjustable neck and modern aesthetic.' },
        { id: 7, name: 'Bluetooth Speaker', price: 89.99, category: 'Electronics', image: '/products/speaker.webp', description: 'Portable Bluetooth speaker with mesh design and high-quality sound.' },
        { id: 8, name: 'Vacuum Cleaner', price: 199.99, category: 'Appliances', image: '/products/odd-vacuum-cleaner.webp', description: 'Futuristic upright vacuum cleaner with a sleek and ergonomic design.' },
        { id: 9, name: 'Smartwatch', price: 149.99, category: 'Electronics', image: '/products/smartwatch.webp', description: 'Modern smartwatch with a sleek design and intuitive interface.' }
    ];
</script>

<div class="max-w-7xl flex flex-wrap justify-between m-auto gap-10 my-10 p-10">

    {#each products.slice(0,3) as product}
        <!-- Card 4 -->
        <a href="/" class="w-80 flex flex-col text-gray-800 hover:scale-[102%] transition-all shadow-xl">
            <img src={product.image} alt={product.description}>

            <div class="flex-grow flex flex-col justify-between p-4">
                <div class="">
                    <div class="flex justify-between">
                        <p class="font-bold">{product.name}</p>
                        <p class="tracking-wide	font-bold text-teal-500">${product.price}</p>
                    </div>
                    
                    <p class="font-extralight text-sm">{product.description}</p>
                </div>

                <div class="flex justify-between items-center mt-4">
                    <button class="bg-yellow-400 py-1 px-4 rounded font-bold w-full">Order Now!</button>
                </div>
            </div>
        </a>
    {/each}

    {#each products.slice(0,3) as product}
        <!-- Card 1 -->
        <a class="group relative w-80 hover:scale-[102%] transition-all cursor-pointer" href="/">
            <img src={product.image} alt={product.description} class="object-cover rounded-t-md">

            <div class="pt-2">
                <div class="flex justify-between item-center">
                    <p class="font-medium bg-gradient-to-r from-red-500 via-orange-500  to-purple-500 bg-clip-text text-transparent">{product.name}</p>
                    <p class="font-bold">${product.price}</p>
                </div>

                <p class="font-light mt-2">{product.description}</p>
            </div>
        </a>
    {/each}

    {#each products.slice(3,6) as product}
        <!-- Card 2 -->
        <a class="w-80 h-[425px] border-2 shadow-xl p-6 rounded-xl bg-gray-50 hover:scale-[102%] bg-gradient-to-b from-gray-100 to-white transition-all text-gray-800" href="/">
            <img src={product.image} alt={product.description} class="rounded-xl"/>

            <div class="mt-2">
                <p class="font-bold text-orange-500">{product.name}</p>
                <p class="font-extralight text-sm">{product.description}</p>
                <p class="mt-4 font-bold tracking-wide">${product.price}</p>
            </div>
        </a>
    {/each}

    {#each products.slice(6,9) as product}
        <!-- Card 3 -->
        <a class="relative w-80 shadow-xl border-[1px] hover:scale-[102%] transition-all group" href="/">
            <div class="absolute p-4 bg-white/70 backdrop-blur-xl group-hover:opacity-20 transition-all">
                <div class="flex justify-between">
                    <p class="font-bold text-green-600">{product.name}</p>
                    <p class="font-bold">${product.price}</p>
                </div>
                <p class="font-extralight text-sm text-justify mt-1">{product.description}</p>
            </div>

            <img src={product.image} alt={product.description} class=""/>
        </a>
    {/each}
</div>