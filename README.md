# Aircraft Size Comparison Renders

Consistent photorealistic studio renders of business aircraft from turboprop to ultra long-range, all matching the same camera angle, lighting, paint, and background.

**Style lock:**
- Pure ivory paint (no markings, livery, logos, text, or registration)
- Single soft champagne rim-light
- Seamless near-black ground with soft reflection
- Gear retracted
- Same three-quarter framing

## Relative scales (length % of Ultra long-range reference)

| Class | Aircraft | Scale |
|-------|----------|-------|
| Turboprop | Beechcraft King Air 350 | 42% |
| Very Light Jet | Cirrus SF50 Vision Jet | 28% |
| Light Jet | Embraer Phenom 300 | 46% |
| Midsize | Cessna Citation XLS+ | 47% |
| Super-midsize | Bombardier Challenger 350 | 62% |
| Heavy | Gulfstream G450 (GIV-SP) | 80% |
| Ultra long-range | Gulfstream G650 family | 100% |

## Files

The full set of renders (individual scaled JPGs + labeled column + scale-check + ZIP) is available as `aircraft_renders.zip` in the project artifacts from the Grok conversation that generated them.

Because the GitHub connector tools used for this automation currently handle text content best for bulk binary uploads, the binary assets have not been bulk-committed here yet. You can:

1. Download `aircraft_renders.zip` from the conversation artifacts.
2. Unzip and `git add` the JPGs + zip into this repo, then push.

Or open a PR with the assets.

### Expected layout after adding assets

```
turbo_scaled.jpg          # King Air 350 @ 42%
vlj_scaled.jpg            # SF50 Vision Jet @ 28%
light_scaled.jpg          # Phenom 300 @ 46%
mid_scaled.jpg            # Citation XLS+ @ 47%
super_scaled.jpg          # Challenger 350 @ 62%
heavy_scaled.jpg          # G450 @ 80%
ultra_scaled.jpg          # G650 @ 100%
aircraft_column_labeled.jpg
scale_check_turbo_ultra.jpg
aircraft_renders.zip
```

Generated with Grok Imagine for visual consistency across the set.

Repo created for Oneways-AI aircraft visual reference work.
