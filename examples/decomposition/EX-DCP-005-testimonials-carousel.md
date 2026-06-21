# EX-DCP-005 — Testimonial Cards / Carousel

Status: active  
Stage: `/decompose`  
Pattern type: testimonial cards, possible slider/carousel  

---

## Synthetic input

A testimonial section contains a heading, several testimonial cards, quote text, customer avatar, name, role/company, star rating, and visible carousel arrows or pagination dots.

---

## Expected decomposition

### 1. Visible Groups

- item: section header  
  role: framing content group  
  evidence: heading introduces the testimonial section  
  confidence: observed

- item: testimonial card group  
  role: repeated social-proof content group  
  evidence: multiple cards contain quotes and customer identity  
  confidence: observed

- item: carousel controls  
  role: possible interactive navigation group  
  evidence: arrows or dots appear near the card group  
  confidence: likely

### 2. Meaningful Content

- item: quote text  
  content_type: testimonial content  
  evidence: card text is presented as customer feedback  
  confidence: observed

- item: avatar, name, role/company  
  content_type: identity metadata  
  evidence: each testimonial includes a person/customer identity block  
  confidence: observed

- item: rating stars  
  content_type: review rating indicator  
  evidence: star icons communicate rating  
  confidence: likely

### 3. Repeated Component Candidates

- component_candidate: testimonial card  
  repeated_parts: quote, avatar, name, role/company, optional rating  
  evidence: same testimonial pattern repeats across cards  
  confidence: observed

### 4. Visual Core

- item: testimonial card set  
  evidence: repeated testimonial cards are the main visible body of the section  
  confidence: observed

### 5. Decoration Layers

- item: quote marks, shadows, card background  
  decorative_function: frame testimonials and add polish  
  evidence: testimonial cards often contain visual quote symbols or card surfaces  
  confidence: likely

### 6. Overlay / Connector Candidates

- item: carousel arrows or pagination dots  
  relationship: attached to the testimonial card group as navigation controls  
  evidence: navigation markers appear near the cards  
  implementation_status: unknown  
  confidence: likely

### 7. Responsive Risks

- risk: carousel behavior cannot be confirmed from static screenshot  
  reason: image may show only one state of an interactive component  
  confidence: observed

- risk: quote length may create uneven card heights  
  reason: testimonials often vary in length  
  confidence: likely

### 8. Unknowns

- unknown: whether the section is a real carousel or static card row  
  why_it_matters: affects later widget/architecture options  
  blocking: no

- unknown: whether avatars are meaningful identity images or decorative thumbnails  
  why_it_matters: affects alt/accessibility decisions  
  blocking: no

### 9. Implementation Assumptions Not Allowed Yet

- assumption: use Testimonial Carousel widget  
  reason: widget choice belongs to `/architectures`

- assumption: use static card containers  
  reason: architecture choice belongs to `/architectures`

Allowed next step:
- `/architectures`
