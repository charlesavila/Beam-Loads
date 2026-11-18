# Planning

Place notes, sketches, and planning documents in this folder.

# Beam Designer Build Plan

## Stage 1: Page mockup and example state

- Create the top-level `index.html` layout only.
- Add labeled sections for beam support, span, loads, member/material selection, beam diagrams, and results.
- Add the example values for a 20 ft simply supported W12x26 beam with one 1 kip/ft uniform load.
- Use placeholder text and static shapes for the beam and diagrams.
- Apply the psychedelic bright-color, flower, rainbow, and abstract-shape visual style.

**Check when done:**

- The full page is readable and usable at desktop and mobile widths.
- The controls and result areas are clearly grouped.
- The example values appear on first load.
- Buttons, focus states, and labels are visible.
- No calculations or pass/fail results are implied.

## Stage 2: Input controls and validation

- Implement support selection, span entry, point-load and uniform-load controls, load add/remove actions, reset, and the calculate action.
- Add member and material selection controls or direct property fields.
- Add validation for required values, span, load locations, ranges, positive properties, and distributed-load start/end order.
- Prevent calculation controls or results from displaying stale or invalid data.

**Check when done:**

- Add, edit, and remove load controls work.
- Invalid fields show adjacent errors.
- Invalid span and load ranges block the output state.
- Reset restores the complete example.
- Calculate and automatic recalculation both behave consistently.

## Stage 3: Reactions, shear, and moment

- Implement support reactions for simply supported beams and cantilevers.
- Implement combined point-load and uniform-load shear and moment functions.
- Draw the beam, support symbols, loads, shear diagram, and moment diagram.
- Add reactions and governing shear/moment values to the result summary.

**Check when done:**

- 20 ft simple beam with 1 kip/ft gives 10 kip reactions and 50 kip-ft maximum moment.
- The cantilever cases give the specified fixed reactions and end moments.
- Partial uniform loads and combined loads update reactions and diagrams.
- Zero loads produce zero reactions, shear, and moment.
- The diagrams show correct signs and load boundaries.

## Stage 4: Deflection and strength checks

- Implement unit-consistent deflection calculations for simple and cantilever beams.
- Add a numerical or analytical maximum-deflection search across the combined loading.
- Draw the deflection diagram and governing deflection value.
- Calculate bending stress and the L/360 limit.
- Implement pass, fail, and invalid result states.

**Check when done:**

- The example beam shows approximately 0.609 in deflection and a 0.667 in limit.
- Cantilever point-load and uniform-load checks reach the correct expected direction and limiting location.
- Bending stress uses kip-ft to ksi conversion correctly.
- The separate bending and deflection checks agree with hand values.
- Invalid inputs do not show calculated or pass/fail results.

## Stage 5: Test cases and final polish

- Verify all specified hand-calculation, invalid-input, reset, add/remove, and zero-load cases.
- Improve labels, accessibility, text alternatives, responsive diagram sizing, and pass/fail presentation.
- Refine the psychedelic visual style while keeping text readable and controls usable.

**Check when done:**

- All hand-calculation cases agree with the displayed rounding.
- Keyboard operation and visible focus work.
- Pass/fail is indicated with text or symbols as well as color.
- Desktop and mobile layouts remain readable.
- The app runs directly through `index.html` with no external assets or build step.
