# EX-DCP-002 — Split Hero with Dashboard Mockup

Status: active  
Stage: `/decompose`  
Pattern type: split hero with copy area and visual mockup  

---

## Synthetic input

A hero section has a left copy column with an eyebrow label, headline, paragraph, and two buttons. The right side contains a large dashboard or app mockup image with floating decorative shapes behind it. The background is light with subtle gradients.

---

## Expected decomposition

### 1. Visible Groups

- item: copy area  
  role: primary content group  
  evidence: left side contains text and CTA buttons  
  confidence: observed

- item: visual mockup area  
  role: visual focal group  
  evidence: right side contains a large dashboard/app image  
  confidence: observed

- item: background atmosphere  
  role: decorative environment  
  evidence: gradients or abstract shapes sit behind content  
  confidence: observed

### 2. Meaningful Content

- item: hero headline and paragraph  
  content_type: primary marketing copy  
  evidence: text explains the section value proposition  
  confidence: observed

- item: CTA buttons  
  content_type: interactive action controls  
  evidence: visible button-like elements appear under the copy  
  confidence: observed

### 3. Repeated Component Candidates

- component_candidate: CTA button  
  repeated_parts: label, button surface, optional icon  
  evidence: two similar buttons appear in the same action group  
  confidence: likely

### 4. Visual Core

- item: dashboard/app mockup  
  evidence: largest visual asset in the section and main visual counterpart to the copy  
  confidence: observed

### 5. Decoration Layers

- item: background gradient or blob shapes  
  decorative_function: add depth and brand atmosphere  
  evidence: abstract visuals appear behind or around the mockup  
  confidence: observed

### 6. Overlay / Connector Candidates

- item: floating badge or decorative shape near mockup  
  relationship: visually attached to the mockup area  
  evidence: small elements appear layered around the mockup  
  implementation_status: unknown  
  confidence: likely

### 7. Responsive Risks

- risk: split layout must stack on smaller screens  
  reason: copy and visual groups may not fit side by side  
  confidence: likely

- risk: decorative shapes may overlap text on mobile  
  reason: background elements are visually positioned around the mockup  
  confidence: likely

### 8. Unknowns

- unknown: whether the mockup is a single image or multiple layered assets  
  why_it_matters: affects later architecture options  
  blocking: no

- unknown: desired mobile ordering of copy vs visual  
  why_it_matters: affects responsive strategy  
  blocking: no

### 9. Implementation Assumptions Not Allowed Yet

- assumption: use two-column Flex  
  reason: architecture choice belongs to `/architectures`

- assumption: position decorative blobs absolutely  
  reason: implementation choice belongs to `/architectures`

Allowed next step:
- `/architectures`
