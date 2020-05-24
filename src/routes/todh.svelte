<script>
  import PageTitle from "../components/PageTitle.svelte";
  import Content from "../components/layouts/Content.svelte";
  import {
    Tabs,
    TabList,
    TabPanel,
    Tab
  } from "../components/molecules/tabs.js";
  import Blockquote from "../components/molecules/Blockquote.svelte";
</script>

<svelte:head>
  <title>Qué es TODH</title>
</svelte:head>

<PageTitle>
  <h1 slot="pagetitle">T-O-D-H</h1>
  <h2 slot="subtitle">Matriz holística de la Creación</h2>
</PageTitle>

<Content>
  <div class="col-desk-8 col-tab-10">
    <h2>Intro</h2>
    <h4>I want to write about my process</h4>
    <p>
      Quisiera en este espacio resumir y sintetizar las lineas generales de un
      proyecto en el que llevo años y que se ha convertido en mi propósito
      vital.
    </p>
    <p>
      Empezó con una crisis existencial que me precipitó a vivir ciertas
      experiencias místicas y reveladoras que se han convertido en un modelo
      holístico de lo que la Creación Es. Un modo de percibir y experimentar la
      contemplación de lo rotundo y de lo misterioso desde una lógica sencilla y
      elemental.
    </p>
    <p>
      No es mi intención sentar ninguna cátedra ni ideología nueva sino más bien
      descubrir y ver a un nivel más profundo lo que ya existe. Nada más. (y
      nada menos...)
    </p>
  </div>
  <div class="col-desk-8 col-tab-10">
    <h3>La matriz 01234</h3>
    <p>
      Todos hemos jugado alguna vez al tetris o por lo menos habremos oído
      hablar, es un juego donde no paran de aparecer objetos que tienden a
      apilarse contra el fondo. El jugador puede mover las formas para que se
      coloquen de una determinada manera mientras caen, cuando la superficie del
      fondo se cubre totalmente de objetos, o sus partes, desaparece.
    </p>
    <p>
      Pues bien, de eso se trata TODH, es lo mismo solo que en un contexto más
      ámplio que se percibe desde la mente abstracta. Digamos que en esto que
      llamamos "la realidad" hay montón de objetos que coinciden en un punto y
      son lo mismo. Darse cuenta de esto es encontrarse de frente con la
      meta-analogía y el lenguaje poético que lo permea todo. Es obvio desde el
      instante en que te das cuenta. Por ejemplo el agua, la sensibilidad, la
      inspiración, la dualidad, la línea, la polaridad, y un infinito número de
      cosas... Cuando se tocan desaparecen, se funden, se fulminan... porque son
      lo mismo. Esta desintegración conceptual permite escarbar en la percepción
      de lo que acontece de una forma ágil y fluida que revela, o por lo menos
      nos aproxima, a su esencia y principio constitutivo.
    </p>
    <p>
      👉 Nota: Estoy tratando de lanzar una serie de ideas que no pretenden ser
      meras disertaciones intelectuales, lo que me interesa es intentar
      transmitir una sensación real y vivenciable. La mirada construye, interpreta, da forma... en cambio la observación simplemente ve.
    </p>
    <p>
      Pitágoras ya lo decía cinco siglos antes de nuestra era, para él sólo
      existía la Unidad. El dos no era 1 + 1 sino 1 dividido en dos partes y el
      tres era el 1 dividido en tres partes... El número para la escuela
      pitagórica era una idea, no sólo una cantidad.
      <strong>1+2+3+4=10=1+0=1</strong>
    </p>
    <div class="col-desk-6 col-tab-8 col-mob-4">
      <Blockquote
        quote="Todo según el número, el peso y la medida"
        author="Platón - Timeo" />
    </div>
    <p>
      Según esto: el sentir o el agua o la dualidad, etc provienen del número
      idea 2. El fuego, la primavera, la intuición, el núcleo de algo, el ser,
      el Sol, etc son instancias, despliegues, extensiones del 1. Así el
      lenguage, un triángulo, el símbolo, el signo géminis y tantas cosas más
      nos retrotraen al número-idea 3. El 4 es el cuaternario, la cruz, la
      tierra, la forma, la materialización, el sentido de realidad, etc. Y por
      último el 0 que origina el propio origen y destino de las cosas, la
      impermanencia, las infinitas posibilidades, el potencial, el Mar de Nun,
      lo incognoscible, etc.
    </p>
    <p>
      La atención del "jugador de TODH" quiero decir "de Tetris" está siempre
      puesta en el fondo y en hacer "desaparecer" el máximo número de objetos,
      no por un afán destructivo persé sino por una necesidad de comprensión de
      "aquello" que es más profunda. La mente concreta siempre va a estar
      proyectando objetos físicos o virtuales, pero la mente abstracta va más
      allá, interpenetra esos objetos, los traspasa, los relaciona, los abarca,
      los comprende... La destrucción creativa es necesaria porque el flujo de
      aparición de objetos es incesante, se amontona y básicamente crea
      problemas. Nunca va a parar, ¡siempre va a haber objetos!.
    </p>
    <p>
      Así que destruir no debería ser un problema cuando estamos conectados con
      el proceso de la Creación misma; la matriz 0-1-2-3-4.
    </p>
    <h3>El orden natural</h3>
    <p>
      Todo es 1 como nada es 0. O como dice el viejo axioma hermético: "como es
      afuera es adentro"
    </p>
  </div>

  <div class="col-desk-6 col-desk-8 col-tab-10 col-mob-4">
    <Tabs>
      <TabList>
        <Tab>Cero</Tab>
        <Tab>Uno</Tab>
        <Tab>Dos</Tab>
        <Tab>Tres</Tab>
        <Tab>Cuatro</Tab>
      </TabList>

      <TabPanel>
        <p>Un campo indeterminado de potencialidad pura. (Fase 0, espacio)</p>
      </TabPanel>

      <TabPanel>
        <p>Una voluntad que decide querer ser (Fase 1, el punto)</p>

      </TabPanel>

      <TabPanel>
        <p>Dualidad, un dentro y un afuera, división (Fase 2, la linea)</p>
      </TabPanel>

      <TabPanel>
        <p>
          Vinculo, razón, conexión de las dos mitades (Fase 3, la superficie)
        </p>
      </TabPanel>

      <TabPanel>
        <p>Materialización, "algo" cristaliza y sucede (Fase 4, el objeto.)</p>
      </TabPanel>
    </Tabs>
  </div>
</Content>
