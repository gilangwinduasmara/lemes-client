<template>
  <div>
    <div class="mt-4">
      <div class="font-bold">Ringkasan</div>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 mt-4">
        <div class="bg-white shadow-sm rounded-md p-4">
          <div class="flex items-center gap-4">
            <div
              class="
                w-8
                h-8
                text-xs
                bg-purple-400
                text-white
                rounded-lg
                flex
                items-center
                justify-center
              "
            >
              <unicon name="book" fill="currentColor"></unicon>
            </div>
            <div class="font-bold">Kelas yang diambil</div>
          </div>
          <div class="mt-4 text-3xl">5</div>
          <div class="font-light">Kelas</div>
        </div>
        <div class="bg-white shadow-sm rounded-md p-4">
          <div class="flex items-center gap-4">
            <div
              class="
                w-8
                h-8
                text-xs
                bg-purple-400
                text-white
                rounded-lg
                flex
                items-center
                justify-center
              "
            >
              <unicon name="award" fill="currentColor"></unicon>
            </div>
            <div class="font-bold">Sertifikat</div>
          </div>
          <div class="mt-4 text-3xl">4</div>
        </div>
        <div
          class="
            bg-purple-800
            shadow-sm
            rounded-md
            p-4
            text-white
            flex
            gap-2
            flex-col
            justify-between
            md:col-span-2
            lg:col-span-1
          "
        >
          <div class="flex items-center gap-4">
            <div class="h-10 w-10 bg-purple-200 rounded-full"></div>
            <div>
              <div class="font-bold">Gilang Windu Asmara</div>
              <div class="font-medium text-blue-200">Student</div>
            </div>
          </div>
          <div class="flex gap-2">
            <div
              class="
                h-8
                w-8
                bg-white
                text-pink-400
                flex
                justify-center
                items-center
                rounded-full
              "
            >
              <unicon name="brain" fill="currentColor"></unicon>
            </div>
            <div
              class="
                h-8
                w-8
                bg-white
                text-blue-400
                flex
                justify-center
                items-center
                rounded-full
              "
            >
              <unicon name="atom" fill="currentColor"></unicon>
            </div>
            <div
              class="
                h-8
                w-8
                bg-white
                text-gray-400
                flex
                justify-center
                items-center
                rounded-full
              "
            >
              <unicon name="graduation-cap" fill="currentColor"></unicon>
            </div>
            <div
              class="
                h-8
                w-8
                bg-white
                text-gray-400
                flex
                justify-center
                items-center
                rounded-full
                text-sm
              "
            >
              2+
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="mt-8">
      <div class="font-bold">Recommended</div>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-12 mt-4">
        <div class="bg-white shadow-sm rounded-xl p-2">
          <div class="bg-yellow-200 w-full h-36 rounded-xl">.</div>
          <div class="p-2">
            <div class="mt-2 font-bold text-xl">Intro to Web Development</div>
            <div class="font-light">Gilang Windu Asmara</div>
            <div class="font-bold">5 Materi</div>
            <a
              href="/course/intro-to-web-development-08312"
              class="
                block
                p-2
                bg-purple-600
                rounded-lg
                text-white text-center
                mt-2
              "
              >Read More</a
            >
          </div>
        </div>
        <div class="bg-white shadow-sm rounded-xl p-2">
          <div class="bg-green-200 w-full h-36 rounded-xl">.</div>
          <div class="p-2">
            <div class="mt-2 font-bold text-xl">Mobile Development</div>
            <div class="font-light">Gilang Windu Asmara</div>
            <div class="font-bold">15 Materi</div>
            <a
              href="/course/intro-to-web-development-08312"
              class="
                block
                p-2
                bg-purple-600
                rounded-lg
                text-white text-center
                mt-2
              "
              >Read More</a
            >
          </div>
        </div>
        <div class="bg-white shadow-sm rounded-xl p-2">
          <div class="bg-red-200 w-full h-36 rounded-xl">.</div>
          <div class="p-2">
            <div class="mt-2 font-bold text-xl">Become a Game Developer</div>
            <div class="font-light">Gilang Windu Asmara</div>
            <div class="font-bold">15 Materi</div>
            <a
              href="/course/intro-to-web-development-08312"
              class="
                block
                p-2
                bg-purple-600
                rounded-lg
                text-white text-center
                mt-2
              "
              >Read More</a
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
