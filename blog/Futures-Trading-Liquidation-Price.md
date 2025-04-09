# **Futures Trading Simulator - Calculating and understanding liquidation price**

📅 *Posted on April 9, 2025*

I built a crypto futures trading simulator that calculates the liquidation price based on the user’s entry price, leverage, and position type (long or short). The core logic is written in Rust for speed and reliability, and it's compiled to WebAssembly (WASM) so it runs directly in the browser. My Next.js + TypeScript frontend loads the WASM module, takes user inputs, and displays the calculated liquidation price in real time.

Breakdown:

Frontend: Next.js + React + Tailwind UI

Core logic: Rust function that computes liquidation price

Rust → WebAssembly: compiled using wasm-pack

Runs in browser: WASM module is loaded dynamically, no server needed

Liquidation logic: simple financial math (entry_price, leverage, maintenance margin)

Reactivity: When user inputs change, React re-calculates and updates UI

## Watch the Video

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe src="https://www.youtube.com/embed/76BrhdWZSZ8" 
          frameborder="0" 
          allowfullscreen 
          style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;">
  </iframe>
</div>

---
## View Code 

[View the project on GitHub](https://github.com/KaylaDefi/Futures_Trading_Sim)

---

## My Commentary

After spending time living vicariously through friends trading perpetual futures contracts, demo trading, and researching these markets, I wanted to make videos that demystify the mechanics and remove some of the hype. It’s easy to get caught up in charts and leverage ratios, but understanding how these tools work is essential to managing risk and making informed decisions.

This led me down a rabbit hole—thinking about not just risk in terms of market volatility, but risk in how we design systems, platforms, and protocols for users.

---

## **Universally Composable Security (MPC Research Continued)**

Inspired by Ran Canetti’s paper, *Universally Composable Security: A New Paradigm for Cryptographic Protocols*.

Universal compasability is designed to rigorously model how cryptographic protocols behave in complex, unpredictable environments—especially when multiple protocols are running at once.

Here are a few core ideas that stood out to me:

- **The Environment Is Watching**: The UC model introduces an environment machine—a formal representation of everything outside the protocol (like other protocols, adversaries, or even users). It can interact with the protocol during execution, not just at the start or end. This models real-world scenarios where side-channel attacks, feedback loops, or concurrent activity happen.

- **Ideal vs. Real**: A protocol π UC-realizes a function f if no environment can distinguish between π (run with a real-world adversary) and an ideal process (with a trusted party and a simulator). This is a much stronger guarantee than traditional definitions.

- **Universal Composition**: The UC theorem says if protocol π securely realizes an ideal functionality F, then any system that uses F as a subroutine can safely replace it with π—even in messy, concurrent, adversarial settings. That’s modularity with real-world teeth.

- **Reactive Functionalities & Adaptive Inputs**: UC handles protocols where inputs and outputs evolve over time—key for trading platforms or smart contracts where one action influences the next.

- **Implications**: This approach offers a formal blueprint for building secure, composable cryptographic systems—whether that’s for privacy-preserving identity, multi-party computation, or financial primitives in DeFi.

If you’re interested in the theoretical side of security—and how it connects to building safer financial tools—stay tuned for more articles covered in the future. 

---

*Thanks for reading (and watching!). If you have questions, thoughts, or feedback—feel free to reach out.*

