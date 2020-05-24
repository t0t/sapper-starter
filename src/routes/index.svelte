<script>
  import PageTitle from "../components/PageTitle.svelte";
  import Content from "../components/layouts/Content.svelte";
  import Button from "../components/atoms/Button.svelte";
  import {
    Tabs,
    TabList,
    TabPanel,
    Tab
  } from "../components/molecules/tabs.js";
</script>

<style>

</style>

<svelte:head>
  <title>TODH wellcome</title>
</svelte:head>

<PageTitle>
  <h1 slot="pagetitle">👋 hola!</h1>
  <h2 slot="subtitle">Esto esto va de arte, diseño front-end y mística</h2>
</PageTitle>

<Content>
  <div class="col-desk-9 col-tab-10 col-mob-4">
    <Tabs>
      <TabList>
        <Tab>Matriz TODH</Tab>
        <Tab>Obra gráfica</Tab>
        <Tab>Prototipado</Tab>
      </TabList>

      <TabPanel>
        <div class="grid-0">
          <div class="col-desk-6">
            <p>
              Proyecto interdisciplinar con el que trato de evanglizar a todo
              aquel incauto que me pregunta.
            </p>
            <Button text="Más info" href="./todh" />
          </div>
          <div class="col-desk-6">
            <img src="img/grafico-1.svg" alt="" />
          </div>
        </div>
      </TabPanel>

      <TabPanel>
        <div class="grid-0">
          <div class="col-desk-6">
            <p>
              Impresiones 3D a partir de matrices generadas por ordenador. Luego
              las trabajo con resina epoxi, cera, arena, etc...
            </p>
            <Button text="Más info" href="./artwork" />
          </div>
          <div class="col-desk-6">
            <img src="img/img3.jpg" alt="" />
          </div>
        </div>

      </TabPanel>

      <TabPanel>
        <p>
          Pasión por el diseño y prototipado UI en el front-end. Avido consumidor de servicios API y fiel aférrimo de las bases de la web: Html, Css/Sass,
          Svelte/Sapper y Git
        </p>

        <pre class="language-html">
          <code class="language-html">
            <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div </span><span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">="</span>md:flex<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag">
              <span class="token tag"><span class="token punctuation">&lt;</span>div</span>
              <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">="</span>md:flex-shrink-0<span class="token punctuation">">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span>
              <span class="token attr-name">class</span>
              <span class="token attr-value">
                <span class="token punctuation">="</span>
                rounded-lg md:w-56
                <span class="token punctuation">"</span>
              </span>
              <span class="token attr-name">src</span>
              <span class="token attr-value">
                <span class="token punctuation">=</span>
                <span class="token punctuation">"</span>
                https://images.unsplash.com/photo-1556740738-b6a63e27c4df?ixlib=rb-1.2.1&amp;ixid=eyJhcHBfaWQiOjEyMDd9&amp;auto=format&amp;fit=crop&amp;w=448&amp;q=80
                <span class="token punctuation">"</span>
              </span>
              <span class="token attr-name">alt</span>
              <span class="token attr-value">
                <span class="token punctuation">="</span>
                Woman paying for a purchase
                <span class="token punctuation">"</span>
              </span>
              <span class="token punctuation">&gt;</span>
            </span>
            <span class="token tag">
              <span class="token punctuation">&lt;/</span>div</span>
              <span class="token punctuation">&gt;</span>
            <span class="token tag">
              <span class="token tag">
                <span class="token punctuation">&lt;</span>
                div
              </span>
              <span class="token attr-name">class</span>
              <span class="token attr-value">
                <span class="token punctuation">=</span>
                <span class="token punctuation">"</span>
                mt-4 md:mt-0 md:ml-6
                <span class="token punctuation">"</span>
              </span>
              <span class="token punctuation">&gt;</span>
            </span>
            <span class="token tag">
              <span class="token tag">
                <span class="token punctuation">&lt;</span>
                div
              </span>
              <span class="token attr-name">class</span>
              <span class="token attr-value">
                <span class="token punctuation">=</span>
                <span class="token punctuation">"</span>
                uppercase tracking-wide text-sm text-indigo-600 font-bold
                <span class="token punctuation">"</span>
              </span>
              <span class="token punctuation">&gt;</span>
            </span>
            Marketing
            <span class="token tag">
              <span class="token tag">
                <span class="token punctuation">&lt;/</span>
                div
              </span>
              <span class="token punctuation">&gt;</span>
            </span>
            <span class="token tag">
              <span class="token tag">
                <span class="token punctuation">&lt;</span>
                a
              </span>
              <span class="token attr-name">href</span>
              <span class="token attr-value">
                <span class="token punctuation">=</span>
                <span class="token punctuation">"</span>
                #
                <span class="token punctuation">"</span>
              </span>
              <span class="token attr-name">class</span>
              <span class="token attr-value">
                <span class="token punctuation">=</span>
                <span class="token punctuation">"</span>
                block mt-1 text-lg leading-tight font-semibold text-gray-900
                hover:underline
                <span class="token punctuation">"</span>
              </span>
              <span class="token punctuation">&gt;</span>
            </span>
            Finding customers for your new business
            <span class="token tag">
              <span class="token tag">
                <span class="token punctuation">&lt;/</span>
                a
              </span>
              <span class="token punctuation">&gt;</span>
            </span>
            <span class="token tag">
              <span class="token tag">
                <span class="token punctuation">&lt;</span>
                p
              </span>
              <span class="token attr-name">class</span>
              <span class="token attr-value">
                <span class="token punctuation">=</span>
                <span class="token punctuation">"</span>
                mt-2 text-gray-600
                <span class="token punctuation">"</span>
              </span>
              <span class="token punctuation">&gt;</span>
            </span>
            Getting a new business off the ground is a lot of hard work. Here
            are five ideas you can use to find your first customers.
            <span class="token tag">
              <span class="token tag">
                <span class="token punctuation">&lt;/</span>
                p
              </span>
              <span class="token punctuation">&gt;</span>
            </span>
            <span class="token tag">
              <span class="token tag">
                <span class="token punctuation">&lt;/</span>
                div
              </span>
              <span class="token punctuation">&gt;</span>
            </span>
            <span class="token tag">
              <span class="token tag">
                <span class="token punctuation">&lt;/</span>
                div
              </span>
              <span class="token punctuation">&gt;</span>
            </span>
          </code>
        </pre>
      </TabPanel>

    </Tabs>
  </div>
</Content>
