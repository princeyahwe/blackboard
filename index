<!doctype html>
<html lang="en">
 <head><script>window["__codeletBootstrap__"]=JSON.parse('{"A":"A","B":"20260731-03-0b60c17","C":{"Abril Fatface":"YACgEZbkUVE,0","Alfa Slab One":"YACgEYS9sJU,0","Anton":"YACgEcYqQ-A,0","Archivo":"YAHO2-t-jNE,0","Arial":"YAGyDvJ_4Ts,0","Bebas Neue":"YACgESME5ew,0","Broken Glyph":"YADZ-exUkv0,0","Canva Sans":"YAFdJjTk5UU,0","Caveat":"YALBs2ploWQ,0","Comic Sans MS":"YAHO2VMiyZo,0","Cormorant Garamond":"YAFdJhX-538,0","Courier New":"YAGzXiGs0_8,0","DM Sans":"YAD1aU3sLnI,0","DM Serif Display":"YAD1aYG82rc,0","Forum":"YACgEcnnqB4,0","Fraunces":"YAEul-FRQw4,0","Georgia":"YAGzXkO0pEM,0","Ghost Mono":"YAHO2EIdDP0,0","Helvetica Neue":"YAFcf6CtJfI,0","Impact":"YAFcfnjI7Vk,0","Inter":"YAFdJvSyp_k,3","Iowan Old Style":"YAGNIFa8j9o,0","Jacques Francois":"YAHO2a5g66Q,0","JetBrains Mono":"YADy3sAhvXQ,0","Oleo Script":"YACgEQQ14jI,0","Playfair Display":"YAFdJhem5V8,1","Poppins":"YAE5fPSY9qM,0","Press Start 2P":"YAFyGr-8pmQ,0","Source Sans 3":"YAG4lO1Mj10,0","Space Grotesk":"YAHO2sjPCSM,0","Times New Roman":"YAGzXW3gftg,0","Times":"YAGzXW3gftg,0","Trebuchet MS":"YAFcfrglpVA,0","Verdana":"YAGzXTctYtQ,0","Work Sans":"YAGXhLOKv44,0","Yellowtail":"YACgEYG4kG4,0"}}');</script><script src="/_sdk/a27874207e105461.telemetry_sdk.js" integrity="sha512-wgI5N9F7oA2h3vH+benMYIv4wGqTct4nKWakqgvfgRyBLmfYq8q/fi6gkfWKd2hMsyN+VQ/qOAOpxybwkcoxlA=="></script>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Online Blackboard</title>
  <script src="https://cdn.tailwindcss.com/3.4.17"></script>
  <script src="https://cdn.jsdelivr.net/npm/lucide@0.263.0/dist/umd/lucide.min.js"></script>
  <script src="/_sdk/935a53bc2e11fb8d.data_sdk.js" integrity="sha512-qr2oyPnEys1WebcOABaRh6hG77r5PWpqeWW6JTKbRJqly/INsfBi31CVNlTmHqjgeLpkVmmHZJUdxSx/32tOFQ=="></script>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&amp;family=Eczar:wght@600;700&amp;display=swap" rel="stylesheet">
  <style>
    :root {
      --chalk: #f8f3de;
      --chalk-muted: #c8d1b3;
      --ink: #14251d;
      --wood: #9a5e31;
    }

    * { box-sizing: border-box; }

    body {
      margin: 0;
      font-family: "DM Sans", sans-serif;
      color: var(--chalk);
      background: #14251d;
    }

    .blackboard-shell {
      width: 100%;
      min-height: calc(100 * min(var(--vh, 1vh), 1vh));
      position: relative;
      overflow-x: hidden;
      background:
        radial-gradient(circle at 14% 8%, rgba(255,255,255,.08) 0 1px, transparent 1.5px),
        radial-gradient(circle at 84% 19%, rgba(255,255,255,.06) 0 1px, transparent 1.5px),
        linear-gradient(135deg, #1c3428 0%, #10271d 56%, #183326 100%);
      background-size: 29px 31px, 37px 41px, auto;
    }

    .blackboard-shell::before {
      content: "";
      position: fixed;
      pointer-events: none;
      inset: 0;
      opacity: .16;
      background-image: repeating-linear-gradient(0deg, transparent 0 3px, rgba(255,255,255,.08) 4px, transparent 5px);
      mix-blend-mode: overlay;
    }

    .chalk-heading {
      font-family: "Eczar", serif;
      letter-spacing: -.025em;
    }

    .wood-frame {
      border: 12px solid var(--wood);
      border-radius: 20px;
      box-shadow: inset 0 0 0 2px rgba(45, 23, 10, .48), 0 20px 45px rgba(0,0,0,.28);
      background:
        radial-gradient(circle at 25% 15%, rgba(255,255,255,.09), transparent 38%),
        #183326;
    }

    .note-board {
      min-height: 510px;
      position: relative;
      overflow: hidden;
      background-image:
        linear-gradient(rgba(232,242,213,.04) 1px, transparent 1px),
        linear-gradient(90deg, rgba(232,242,213,.04) 1px, transparent 1px);
      background-size: 32px 32px;
    }

    .sticky-note {
      position: absolute;
      width: min(220px, 42vw);
      min-height: 150px;
      padding: 18px 17px 15px;
      border: 1px solid rgba(50, 45, 23, .18);
      border-radius: 3px 4px 10px 3px;
      box-shadow: 5px 8px 13px rgba(0,0,0,.28);
      color: #2d2b20;
      cursor: grab;
      touch-action: none;
      transition: box-shadow .18s ease, transform .18s ease;
      transform: rotate(var(--tilt, -1deg));
      user-select: none;
    }

    .sticky-note:hover,
    .sticky-note:focus-within {
      box-shadow: 8px 12px 19px rgba(0,0,0,.35);
      z-index: 5;
    }

    .sticky-note.dragging {
      cursor: grabbing;
      transform: rotate(0deg) scale(1.03);
      z-index: 30;
      transition: none;
    }

    .sticky-note::after {
      content: "";
      position: absolute;
      right: 13px;
      bottom: 10px;
      width: 56px;
      height: 8px;
      opacity: .17;
      background: linear-gradient(120deg, transparent 10%, #615a32 11% 15%, transparent 16% 27%, #615a32 28% 31%, transparent 32%);
    }

    .note-content {
      white-space: pre-wrap;
      overflow-wrap: anywhere;
      line-height: 1.38;
      font-weight: 600;
      font-size: .94rem;
      padding-right: 4px;
    }

    .delete-actions button {
      font-size: .7rem;
      line-height: 1;
      border-radius: 999px;
      padding: .38rem .55rem;
      font-weight: 700;
      transition: transform .15s ease, opacity .15s ease;
    }

    .delete-actions button:hover { transform: translateY(-1px); }

    .form-control {
      width: 100%;
      border: 1px solid rgba(224, 238, 202, .34);
      border-radius: 10px;
      padding: .72rem .8rem;
      background: rgba(8, 22, 15, .46);
      color: var(--chalk);
      outline: none;
      transition: border-color .18s ease, box-shadow .18s ease;
    }

    .form-control::placeholder { color: #afbaa4; opacity: 1; }

    .form-control:focus {
      border-color: #e4d17c;
      box-shadow: 0 0 0 3px rgba(228, 209, 124, .17);
    }

    select.form-control option { color: #13261c; }

    .post-button {
      box-shadow: 0 5px 0 rgba(57, 40, 12, .75);
      transition: transform .15s ease, box-shadow .15s ease, opacity .15s ease;
    }

    .post-button:hover { transform: translateY(-2px); box-shadow: 0 7px 0 rgba(57, 40, 12, .75); }
    .post-button:active { transform: translateY(3px); box-shadow: 0 2px 0 rgba(57, 40, 12, .75); }
    .post-button:disabled { opacity: .65; cursor: wait; transform: none; }

    .status-message { min-height: 1.25rem; }

    @media (max-width: 640px) {
      .wood-frame { border-width: 8px; border-radius: 15px; }
      .note-board { min-height: 590px; }
      .sticky-note { width: min(190px, 65vw); }
    }
  </style>
  <script src="/_sdk/6030e540d4419216.resizing_sdk.js" type="text/javascript" integrity="sha512-b5KWzyoXsbWP4smq4sftIi6Kts4YVBpBsz0BwCViwbBJkK64a3/Z6ZMdWA+qnplNcXw4mhZeqvQi3mOosiRJdA=="></script>
 </head>
 <body data-template-id="__page-root">
  <div class="blackboard-shell">
   <header data-template-id="board-header" class="canva-header border-b border-[#dce8c940] bg-[#0e2118cc]">
    <div class="mx-auto flex w-full max-w-6xl items-center gap-3 px-5 py-5 sm:px-8">
     <div class="flex h-11 w-11 shrink-0 items-center justify-center rounded-full border border-[#e4d17c88] bg-[#e4d17c] text-[#183326]"><i data-lucide="message-square-plus" aria-hidden="true" class="h-5 w-5"></i>
     </div>
     <div>
      <h1 data-template-id="board-title" class="canva-text chalk-heading text-3xl font-bold leading-none sm:text-4xl"></h1>
      <p data-template-id="board-subtitle" class="canva-text mt-1 text-sm font-medium"></p>
     </div>
    </div>
   </header>
   <main class="mx-auto w-full max-w-6xl px-5 py-8 sm:px-8 sm:py-10">
    <section data-template-id="post-panel" class="canva-panel mb-8 rounded-2xl border border-[#dce8c940] bg-[#274535e8] p-5 shadow-xl shadow-black/10 sm:p-6" aria-labelledby="composer-heading">
     <div class="mb-5 flex items-start gap-3"><i data-lucide="pencil-line" aria-hidden="true" class="mt-1 h-5 w-5 text-[#e4d17c]"></i>
      <div>
       <h2 id="composer-heading" class="chalk-heading text-xl font-semibold text-[#f8f3de]">Add your answer</h2>
       <p class="mt-1 text-sm text-[#c8d1b3]">Share a thought with everyone viewing this board.</p>
      </div>
     </div>
     <form id="note-form">
      <div class="grid gap-4 md:grid-cols-[1fr_190px]">
       <div><label data-template-id="answer-label" class="canva-text mb-2 block text-sm font-semibold" for="answer-input"></label> <textarea data-template-id="answer-input" class="canva-input form-control min-h-[104px] resize-y" id="answer-input" maxlength="350" required></textarea>
       </div>
       <div class="grid content-start gap-4 sm:grid-cols-2 md:grid-cols-1">
        <div><label data-template-id="name-label" class="canva-text mb-2 block text-sm font-semibold" for="name-input"></label> <input data-template-id="name-input" class="canva-input form-control" id="name-input" type="text" maxlength="40">
        </div>
        <div><label data-template-id="color-label" class="canva-text mb-2 block text-sm font-semibold" for="color-input"></label> <select id="color-input" class="form-control" aria-label="Sticky note color"> <option value="#f6dc70">Sunny yellow</option> <option value="#f6a6a6">Coral pink</option> <option value="#9ed7b1">Mint green</option> <option value="#9fc8ee">Sky blue</option> <option value="#d5b8ec">Lavender</option> </select>
        </div>
       </div>
      </div>
      <div class="mt-5 flex flex-wrap items-center justify-between gap-3">
       <p id="form-status" class="status-message text-sm text-[#dce8c9]" aria-live="polite"></p><button data-template-id="post-button" class="canva-button post-button inline-flex items-center gap-2 rounded-lg px-5 py-3 font-bold focus:outline-none focus:ring-4 focus:ring-[#e4d17c66]" type="submit"> <i data-lucide="pin" aria-hidden="true" class="h-4 w-4"></i> </button>
      </div>
     </form>
    </section>
    <section data-template-id="board-section" class="canva-section wood-frame" aria-labelledby="board-heading">
     <div class="flex flex-wrap items-end justify-between gap-3 px-5 pt-5 sm:px-7 sm:pt-6">
      <div>
       <h2 data-template-id="board-heading" class="canva-text chalk-heading text-2xl font-semibold"></h2>
       <p data-template-id="board-helper" class="canva-text mt-1 text-sm"></p>
      </div>
      <div id="note-count" class="rounded-full border border-[#dce8c940] bg-[#10271da8] px-3 py-1 text-xs font-semibold text-[#dce8c9]" aria-live="polite">
       Loading notes…
      </div>
     </div>
     <div id="note-board" class="note-board mt-4" aria-live="polite">
      <div id="empty-state-wrap" class="flex min-h-[510px] items-center justify-center px-5 text-center">
       <p data-template-id="empty-board" class="canva-text max-w-sm text-lg font-medium"></p>
      </div>
     </div>
    </section>
   </main>
   <footer class="mx-auto w-full max-w-6xl px-5 pb-8 text-center sm:px-8">
    <p data-template-id="footer-note" class="canva-text text-sm"></p>
   </footer>
   <template id="sticky-note-template">
    <article data-template-id="sticky-note" class="canva-card sticky-note" tabindex="0">
     <p class="note-content"></p>
     <div class="mt-4 flex items-end justify-between gap-2">
      <div>
       <p data-template-id="sticky-author" class="canva-text note-author text-xs font-bold"></p>
       <p data-template-id="sticky-date" class="canva-text note-date mt-0.5 text-[.68rem]"></p>
      </div>
      <div class="delete-actions flex items-center gap-1"><button data-template-id="delete-note-button" class="canva-button delete-trigger" type="button"></button>
       <div class="confirm-controls hidden items-center gap-1"><button data-template-id="confirm-delete-button" class="canva-button confirm-delete" type="button"></button> <button data-template-id="cancel-delete-button" class="canva-button cancel-delete" type="button"></button>
       </div>
      </div>
     </div>
    </article>
   </template>
  </div>
  <script src="/_sdk/9a740ce6cacd0808.editing_sdk.js" integrity="sha512-ZcKE2UXVxSh0Kmty64HdB2xjpgsalbehms1KOXHeK7POjO9v81VU+RYWmq0cOBM9u4mY5oRq7UsigAanNH4Iww=="></script>
  <script>
    const board = document.getElementById("note-board");
    const form = document.getElementById("note-form");
    const answerInput = document.getElementById("answer-input");
    const nameInput = document.getElementById("name-input");
    const colorInput = document.getElementById("color-input");
    const statusEl = document.getElementById("form-status");
    const submitButton = form.querySelector("button[type='submit']");
    const countEl = document.getElementById("note-count");
    const emptyWrap = document.getElementById("empty-state-wrap");
    let records = [];
    let isReady = false;

    function setStatus(message, type) {
      statusEl.textContent = message;
      statusEl.className = "status-message text-sm " + (type === "error" ? "text-[#ffb2a8]" : "text-[#dce8c9]");
    }

    function formatDate(iso) {
      const date = new Date(iso);
      return Number.isNaN(date.getTime()) ? "" : date.toLocaleDateString(undefined, { month: "short", day: "numeric" });
    }

    function clampPosition(value, max) {
      return Math.max(1, Math.min(max, value));
    }

    function updateNoteElement(el, record) {
      const x = clampPosition(Number(record.pos_x) || 8, 96);
      const y = clampPosition(Number(record.pos_y) || 9, 88);
      el.dataset.recordId = record.__backendId;
      el.style.left = x + "%";
      el.style.top = y + "%";
      el.style.background = record.color || "#f6dc70";
      el.style.setProperty("--tilt", ((x + y) % 5 - 2) + "deg");
      el.querySelector(".note-content").textContent = record.content || "";
      el.querySelector(".note-author").textContent = record.author_name ? "— " + record.author_name : "— Anonymous";
      el.querySelector(".note-date").textContent = formatDate(record.created_at);
      el.setAttribute("aria-label", "Sticky note: " + (record.content || "Untitled note"));
    }

    function createNoteElement(record) {
      const fragment = document.getElementById("sticky-note-template").content.cloneNode(true);
      const note = fragment.querySelector(".sticky-note");
      updateNoteElement(note, record);

      const deleteTrigger = note.querySelector(".delete-trigger");
      const confirmControls = note.querySelector(".confirm-controls");
      deleteTrigger.addEventListener("click", (event) => {
        event.stopPropagation();
        deleteTrigger.classList.add("hidden");
        confirmControls.classList.remove("hidden");
        confirmControls.classList.add("flex");
      });

      note.querySelector(".cancel-delete").addEventListener("click", (event) => {
        event.stopPropagation();
        confirmControls.classList.add("hidden");
        confirmControls.classList.remove("flex");
        deleteTrigger.classList.remove("hidden");
      });

      note.querySelector(".confirm-delete").addEventListener("click", async (event) => {
        event.stopPropagation();
        const current = records.find(item => item.__backendId === record.__backendId);
        if (!current) return;
        confirmControls.querySelectorAll("button").forEach(button => button.disabled = true);
        const result = await window.dataSdk.delete(current);
        if (!result.isOk) {
          confirmControls.querySelectorAll("button").forEach(button => button.disabled = false);
          setStatus("That note could not be removed. Please try again.", "error");
        }
      });

      attachDrag(note);
      return note;
    }

    function renderNotes(data) {
      records = data.slice();
      const existing = new Map(
        [...board.querySelectorAll(".sticky-note")].map(element => [element.dataset.recordId, element])
      );

      data.forEach(record => {
        const existingNote = existing.get(record.__backendId);
        if (existingNote) {
          if (!existingNote.classList.contains("dragging")) updateNoteElement(existingNote, record);
          existing.delete(record.__backendId);
        } else {
          board.appendChild(createNoteElement(record));
        }
      });

      existing.forEach(element => element.remove());
      emptyWrap.classList.toggle("hidden", data.length > 0);
      countEl.textContent = data.length === 1 ? "1 answer posted" : data.length + " answers posted";
      if (data.length >= 999) setStatus("The board is full. Delete a note before adding another.", "error");
    }

    function attachDrag(note) {
      let startX = 0, startY = 0, baseLeft = 0, baseTop = 0;

      note.addEventListener("pointerdown", (event) => {
        if (event.target.closest("button")) return;
        startX = event.clientX;
        startY = event.clientY;
        baseLeft = parseFloat(note.style.left) || 8;
        baseTop = parseFloat(note.style.top) || 8;
        note.classList.add("dragging");
        note.setPointerCapture(event.pointerId);
      });

      note.addEventListener("pointermove", (event) => {
        if (!note.classList.contains("dragging")) return;
        const rect = board.getBoundingClientRect();
        const nextX = clampPosition(baseLeft + ((event.clientX - startX) / rect.width) * 100, 94);
        const nextY = clampPosition(baseTop + ((event.clientY - startY) / rect.height) * 100, 88);
        note.style.left = nextX + "%";
        note.style.top = nextY + "%";
      });

      note.addEventListener("pointerup", async (event) => {
        if (!note.classList.contains("dragging")) return;
        note.classList.remove("dragging");
        const record = records.find(item => item.__backendId === note.dataset.recordId);
        if (!record) return;

        const updated = {
          ...record,
          pos_x: String(parseFloat(note.style.left)),
          pos_y: String(parseFloat(note.style.top))
        };
        const result = await window.dataSdk.update(updated);
        if (!result.isOk) {
          updateNoteElement(note, record);
          setStatus("The note position could not be saved.", "error");
        }
        if (note.hasPointerCapture(event.pointerId)) note.releasePointerCapture(event.pointerId);
      });
    }

    form.addEventListener("submit", async (event) => {
      event.preventDefault();
      const content = answerInput.value.trim();
      if (!content) {
        setStatus("Please write an answer before posting.", "error");
        answerInput.focus();
        return;
      }
      if (!isReady) {
        setStatus("The board is still loading. Please try again in a moment.", "error");
        return;
      }
      if (records.length >= 999) {
        setStatus("The board is full. Delete a note before adding another.", "error");
        return;
      }

      submitButton.disabled = true;
      setStatus("Pinning your answer to the board…");
      const result = await window.dataSdk.create({
        content,
        author_name: nameInput.value.trim(),
        color: colorInput.value,
        pos_x: String(5 + Math.random() * 72),
        pos_y: String(7 + Math.random() * 65),
        created_at: new Date().toISOString()
      });

      submitButton.disabled = false;
      if (result.isOk) {
        form.reset();
        colorInput.value = "#f6dc70";
        setStatus("Your answer is now on the board.");
        answerInput.focus();
      } else {
        setStatus("Your answer could not be posted. Please try again.", "error");
      }
    });

    async function initializeBoard() {
      const handler = {
        onDataChanged(data) {
          renderNotes(data);
        }
      };
      const result = await window.dataSdk.init(handler);
      if (result.isOk) {
        isReady = true;
        setStatus("Ready for your answer.");
      } else {
        setStatus("The board could not connect. Refresh and try again.", "error");
        countEl.textContent = "Board unavailable";
      }
    }

    document.addEventListener("DOMContentLoaded", () => {
      lucide.createIcons();
      initializeBoard();
    });
  </script>
 </body>
</html>
