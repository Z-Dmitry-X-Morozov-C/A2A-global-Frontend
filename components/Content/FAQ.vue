<template>
  <section>
    <div class="faq__title">
      <h1 class="faq__title-text">Frequently asked questions</h1>
    </div>

    <div v-for="item in 4" class="accordion">
      <details class="accordion__item" name="faq">
        <summary class="accordion__summary">
          <span class="accordion__summary-title" role="term" aria-details="faq-1"> What is A2A.Global? </span>
        </summary>
      </details>

      <div class="accordion__content" id="faq-1" role="definition">
        <div class="accordion__content-body">
          <p>
            A2A.Global is a payments processing company that revolutionises how payments are made. We believe that card
            payments are the artifacts of the past, and direct account-to-account bank payments via simple buy fast
            button are modernising the payment industry and client habits
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.faq__title {
  font-size: calc(28px + (20 + 20 * 0.7) * (100vw - 375px) / 1920);
  letter-spacing: -1px;
  font-weight: 600;
  text-align: center;
  margin-bottom: 40px;
}

.accordion {
  padding: 20px;
  border-radius: 24px;
  background-color: #f2f2f2;
  margin-bottom: 16px;
}

.accordion__content {
  display: grid;
  grid-template-rows: 0fr;
  align-self: end;
  transition: all 0.2s ease-in-out;
}

.accordion__content-body {
  overflow: hidden;
}

.accordion__content-body > p {
  margin-top: 20px;
}

.accordion__item[open] + .accordion__content {
  grid-template-rows: 1fr;
  margin-bottom: 20px;
}

details {
  position: relative;
}

summary {
  list-style: none;
  cursor: pointer;
}

details summary::before {
  content: "›";
  font-size: 24px;
  transform: rotate(180deg);
  position: absolute;
  right: 0;
  top: -3px;
  transition: all 0.1s ease-in;
}

details[open] summary::before {
  content: "›";
  rotate: -90deg;
}
</style>
