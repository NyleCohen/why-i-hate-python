<template>
  <v-app>
    <v-app-bar app color="black" dark>
      <div class="d-flex align-center">
        <v-img
          alt="Python Logo"
          class="shrink mr-2"
          contain
          src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c3/Python-logo-notext.svg/768px-Python-logo-notext.svg.png"
          transition="scale-transition"
          width="40"
        />

        <h1>Why I hate Python</h1>
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://www.hackerfactor.com/blog/index.php?/archives/825-8-Reasons-Python-Sucks.html"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <a href="https://python.org">
        <v-img
          lazy-src="https://www.ortho-spine.com/application/files/thumbnails/small/4415/6009/7144/Spine-Pain-Causes94790.jpg"
          max-height="450"
          max-width="350"
          src="https://www.ortho-spine.com/application/files/thumbnails/small/4415/6009/7144/Spine-Pain-Causes94790.jpg"
          class="justify-center"
        ></v-img>
      </a>

      <v-simple-table>
        <template v-slot:default>
          <thead>
            <tr>
              <th class="text-left">Number</th>
              <th class="text-left">Reasons Why I Hate Python</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>1</td>
              <td>Interpreted language = really slow</td>
            </tr>
            <tr>
              <td>2</td>
              <td>Clunky syntax</td>
            </tr>
            <tr>
              <td>3</td>
              <td>PiP sucks</td>
            </tr>
            <tr>
              <td>4</td>
              <td>Code changing API changes every version</td>
            </tr>
            <tr>
              <td>5</td>
              <td>Included are disgousting</td>
            </tr>
          </tbody>
        </template>
      </v-simple-table>

      <div class="text-center">
        <v-bottom-sheet v-model="sheet" inset>
          <template v-slot:activator="{ on, attrs }">
            <v-btn color="orange" dark v-bind="attrs" v-on="on">
              Click Me!
            </v-btn>
          </template>
          <v-sheet class="text-center" height="200px">
            <v-btn class="mt-6" text color="error" @click="sheet = !sheet">
              close
            </v-btn>
            <div class="my-3">
              Occasionally I go out to lunch with some of my techie friends and
              we have a great time geeking together. Inevitably, the discussion
              will turn to programming languages. One might lament "I have to
              modify some Java code. I hate Java. (Oh, sorry, Kyle.)" (It
              probably doesn't help that we gave Kyle the nickname "Java-boy"
              over a decade ago.) Another will gripe about some old monolithic
              shell code that nobody wants to rewrite. And me, well... I just
              blurted it out: I hate Python. I hate it with a passion. If I have
              the choice between using some pre-existing Python code or
              rewriting it in C, I'd rather rewrite it in C. When I finished
              shouting, Bill humorously added, "But what do you really think
              about Python?" So I'm dedicating this to Bill. Here's my list of
              "8 reasons Python sucks".
            </div>
          </v-sheet>
        </v-bottom-sheet>
      </div>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    sheet: false,
  }),
};
</script>
