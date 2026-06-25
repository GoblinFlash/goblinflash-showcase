# Safety Boundaries

This showcase describes boundaries, not operational procedures.

## No Write Authority

GoblinFlash public documentation must not create, imply, or advertise firmware write authority.

Do not include:

- flashing commands
- NVRAM write procedures
- setup_var usage
- flashrom recipes
- H2OUVE workflows
- SPI write guidance
- patch application steps
- unlock recipes

## No Private Material

Do not include:

- firmware dumps
- BIOS dump material
- SPI dump material
- private case data
- private identifiers
- customer logs
- generated experiment artifacts
- vulnerable fixture files

## No Device-Specific Procedures

The public showcase may discuss architecture and safety rules. It must not provide device-specific offsets, vendor-specific exploit guidance, or model-specific recovery instructions.

## Discussion Boundaries

Future Discussions, if enabled, are for controlled architecture and research discussion only. Issues remain intentionally disabled until a separate governance decision changes that.

Out-of-scope discussion topics include support requests, unlock requests, dump analysis, patch requests, and write-path guidance.
