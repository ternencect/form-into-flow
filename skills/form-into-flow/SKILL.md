---
name: form-into-flow
description: Transform images into Form into Flow abstract paintings, combining recognizable anchors, flowing color layers, fine ink lines, and open space. Use when the user requests Form into Flow or explicitly invokes this skill. Derive the palette from the input; not intended for ordinary filters or realistic oil-painting conversions.
---

# Form into Flow

Preserve the input's identifying features while reshaping its main forms, surroundings, and paint into a unified space. The style depends on structural transformation, contrasts in detail density, and shifts between defined and dissolved edges. Shrinking the subject, clearing the background, adding ribbons, or applying texture alone is insufficient.

Form into Flow is a working style definition, not an attribution to an established movement, artist, or physical medium.

## Plan the composition

Inspect the input and read the [style guide](references/style-guide.md). Locate these decisions in specific areas of the image:

- **Recognition anchors:** Preserve identity, pose, essential counts, necessary structures, and user-specified elements. Distinguish these from original size, proportions within the frame, and incidental detail. Do not invent unseen anatomy or functional structures.
- **Structural transformation:** Choose a major form and a primary action, such as compression, extension, dissolution, or disruption of perspective. Follow the input's contours, ground contact, shadows, or reflections to change spatial relationships.
- **Density and hierarchy:** Identify a continuous quiet area beside a concentration of detail. Scale the subject to suit the image rather than always making it tiny. When a face must remain large, establish contrast through the surrounding space.
- **Color and material:** Extract broad color fields, structural darks, and concentrated highlights from the input; redistribute their area and intensity. Combine transparent and opaque layers, dark nodes, dragged marks, and fine lines as needed. Keep texture subordinate to structure and preserve dark values in night scenes.

By default, preserve aspect ratio, subject identity, essential counts, and existing transparency while allowing secondary forms and space to change. Honor requests to preserve form and explain the resulting limits on abstraction; do not demand both exhaustive fidelity and complete deconstruction.

For people, animals, or results with detached subjects, decorative ribbons, or uniform heavy texture, consult [failure cases](references/failure-cases.md).

## Prompt and generate

Describe spatial relationships first, followed by protected features, color, and local materials. Use this outline as needed:

> Transformation and composition; how the main form changes; quiet and concentrated areas; required features; distribution of source colors; structural changes in edges and materials; a few relevant exclusions.

Resolve conflicts between preservation, subject scale, and abstraction before generating. Material terms cannot replace spatial design. Avoid accumulating exclusions from previous attempts. Gradients, long curves, thin washes, and local texture are valid options; do not impose a standard S-curve, cliff, ribbon, blue-pink palette, or right-aligned subject.

Use the built-in `image_gen` tool and follow the available imagegen skill. Inspect local inputs before passing them through the tool's supported file-path or conversation-image mechanism. State each attachment's role. By default, pass only the current source image and save outputs separately without overwriting it.

This skill includes no reference images and depends on no specific local directory. The user supplies the input. Use additional style references only when explicitly designated by the user, and avoid reproducing watermarks.

## Review and iterate

Review the whole image first: do recognition anchors, structural boundaries, color fields, and gestures form one space? If an intact realistic subject still looks pasted onto a background, with surrounding ribbons or ink lines that could be removed independently, local improvements do not establish success.

Apply the guide's five criteria: **structural transformation, density contrast, recognition anchors, material and structure, and color organization**. Provide observable evidence and specific shortcomings rather than subjective scores. If transformation or density contrast fails, record that failure. Passing an assistant's visual review does not establish user approval.

Generate one image by default. For a clear local defect, make at most one targeted revision and retain both versions and their full prompts. For requested batches, follow the requested scope, hold the skill version and shared rules constant, and retain failed outputs. Reconsider the design after recurring deviations or negative feedback instead of automatically cycling through prompt variations.

Deliver the image and its location. Distinguish file validation, assistant visual review, and user approval. State remaining shortcomings; do not automatically make a single result a reference for future tasks.

## Limitations

Relationships that work in landscapes may not transfer to people or animals. Check identity, anatomy, and spatial integration for the current input without claiming reliable results across all subjects. Read [evaluation limits](references/evidence-status.md) when discussing suitability or validation.
