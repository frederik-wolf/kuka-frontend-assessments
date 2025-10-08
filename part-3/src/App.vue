<script setup>
import { ref } from 'vue';

const products = ref([
  {
    id: 1,
    title: "KR CYBERTECH nano",
    image:
      "https://www.kuka.com/-/media/kuka-corporate/images/products/robots/kr-cybertech/kr-cybertech_nano_2.jpg?rev=a5468246ffab4b27990c2481b8c60946&w=767",
    alt: "KR CYBERTECH nano",
    description:
      "Beste Performance bei hoher Leistungsdichte: Die spezialisierten Prozessroboter der Produktfamilie KR CYBERTECH nano sind perfekt auf das Handhaben kleiner Bauteile abgestimmt.",
    tags: ["High Precision", "Ceiling-mountable"],
  },
  {
    id: 2,
    title: "KR FORTEC PA",
    image:
      "https://www.kuka.com/-/media/kuka-corporate/images/products/robots/kr-fortec/kr-fortec-pa/kr-470-r3200-2-pa_teaser.jpg?rev=c38aadff5d2d4c99a7c977280cba01a7&w=767",
    alt: "KR FORTEC PA",
    description:
      "Der KR FORTEC PA ist ein Palettierroboter, der nicht nur durch seine hohe Leistung überzeugt, sondern auch durch besonders niedrige Betriebskosten. Aufgrund seines schlanken Designs ist er äußerst wendig.",
    tags: ["High Payload", "Low TCO"],
  },
  {
    id: 3,
    title: "KR TITAN ultra",
    image:
      "https://www.kuka.com/-/media/kuka-corporate/images/products/robots/kr-titan-ultra/kr-titan-ultra-robot.jpg?rev=427251f3f6114dad9ce79cd6e114af54&w=767",
    alt: "KR TITAN ultra",
    description:
      "Der Spezialist für das Handling im hohen Schwerlast-Bereich: Der Industrieroboter bewegt Nutzlasten bis zu 1500 kg und erzielt er mit seinem geringen Eigengewicht hohe Reichweiten.",
    tags: ["Auotmotive", "High Payload"],
  },
]);
</script>

<template>
  <div class="container space-y-8">
    <div class="flex w-full justify-end">
      <button class="bg-primary text-white px-4 py-2 rounded-md hover:bg-primary-600">Add Product</button>
    </div>

    <div class="grid sm:grid-cols-2 md:grid-cols-3 gap-x-4 gap-y-8">
      <div>
        <div class="aspect-4/3 mb-4">
          <img 
            src="https://www.kuka.com/-/media/kuka-corporate/images/products/robots/kr-cybertech/kr-cybertech_nano_2.jpg?rev=a5468246ffab4b27990c2481b8c60946&w=767"
            alt="KR CYBERTECH nano"
            class="w-full h-full object-cover"
          />
        </div>
        <div>
          <h3 class="text-xl font-bold mb-1">KR CYBERTECH nano</h3>
          <p class="text-base text-gray-500 mb-3">Beste Performance bei hoher Leistungsdichte: Die spezialisierten Prozessroboter der Produktfamilie KR CYBERTECH nano sind perfekt auf das Handhaben kleiner Bauteile abgestimmt.</p>
          <div class="flex flex-wrap gap-2">
            <span class="bg-gray-200 text-xs p-1">High Precision</span>
            <span class="bg-gray-200 text-xs p-1">Ceiling-mountable</span>
          </div>
        </div>
      </div>
      <div>
        <div class="aspect-4/3 mb-4">
          <img 
            src="https://www.kuka.com/-/media/kuka-corporate/images/products/robots/kr-fortec/kr-fortec-pa/kr-470-r3200-2-pa_teaser.jpg?rev=c38aadff5d2d4c99a7c977280cba01a7&w=767"
            alt="KR FORTEC PA"
            class="w-full h-full object-cover"
          />
        </div>
        <div>
          <h3 class="text-xl font-bold mb-1">KR FORTEC PA
          </h3>
          <p class="text-base text-gray-500 mb-3">Der KR FORTEC PA ist ein Palettierroboter, der nicht nur durch seine hohe Leistung überzeugt, sondern auch durch besonders niedrige Betriebskosten. Aufgrund seines schlanken Designs ist er äußerst wendig.</p>
          <div class="flex flex-wrap gap-2">
            <span class="bg-gray-200 text-xs p-1">High Payload</span>
            <span class="bg-gray-200 text-xs p-1">Low TCO</span>
          </div>
        </div>
      </div>
      <div>
        <div class="aspect-4/3 mb-4">
          <img 
            src="https://www.kuka.com/-/media/kuka-corporate/images/products/robots/kr-titan-ultra/kr-titan-ultra-robot.jpg?rev=427251f3f6114dad9ce79cd6e114af54&w=767"
            alt="KR TITAN ultra"
            class="w-full h-full object-cover"
          />
        </div>
        <div>
          <h3 class="text-xl font-bold mb-1">KR TITAN ultra</h3>
          <p class="text-base text-gray-500 mb-3">Der Spezialist für das Handling im hohen Schwerlast-Bereich: Der Industrieroboter bewegt Nutzlasten bis zu 1500 kg und erzielt er mit seinem geringen Eigengewicht hohe Reichweiten.</p>
          <div class="flex flex-wrap gap-2">
            <span class="bg-gray-200 text-xs p-1">Auotmotive</span>
            <span class="bg-gray-200 text-xs p-1">High Payload</span>
          </div>
        </div>
      </div>
    </div>
  </div>


  <div class="hidden bg-white absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 p-4 border max-w-[60vw] w-full max-h-[80vh] overflow-y-auto">
    <h2 class="text-2xl font-bold mb-4">Add Product</h2>
    
    <form class="space-y-4">
      <div>
        <label class="block mb-1">Image:</label>
        <input type="text" name="image" class="w-full p-2 border rounded" />
      </div>
      <div>
        <label class="block mb-1">Title:</label>
        <input type="text" name="title" class="w-full p-2 border rounded" />
      </div>
      <div>
        <label class="block mb-1">Description:</label>
        <textarea name="description" class="w-full p-2 border rounded"></textarea>
      </div>
      <div>
        <label class="block mb-1">Tags:</label>
        <input type="text" name="tags" class="w-full p-2 border rounded" />
      </div>
      
      <div class="flex justify-between pt-4">
        <button type="button" class="bg-gray-500 text-white px-4 py-2 rounded-md hover:bg-gray-600">Close</button>
        <button type="submit" class="bg-primary text-white px-4 py-2 rounded-md hover:bg-primary-600">Submit</button>
      </div>
    </form>
  </div>
</template>
