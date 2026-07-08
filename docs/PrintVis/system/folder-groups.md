# Folder Groups

Folder Groups in PrintVis manage the automatic creation and organization of folders (typically in SharePoint) for production jobs. When a case reaches a specific Status Code that has folder creation enabled, PrintVis can automatically create a structured folder hierarchy for the job's files.

## Usage

Folder Groups are used to:
- Define which folders are created when a job enters production
- Organize job files in SharePoint (or other document management systems)
- Ensure consistent folder structure across all jobs
- Link digital assets to specific jobs

### Folder Archive

When a case is archived (based on the Status Code configured in General Setup), the associated folders can be moved to an archive location. The **Folder Archive Status Code** and **Folder Archive Days Delayed** settings in General Setup control this behavior.

## Setup

Folder Groups are found by searching **PrintVis Folder Groups**.

!!! warning "Missing Content"
    Detailed setup documentation for Folder Groups is not fully available in the current source material. Refer to the legacy Folder Groups documentation (Legacy/System/FolderGroups.md) for configuration details.

## Examples

!!! warning "Missing Content"
    No specific Folder Groups examples are currently documented.

## See Also

- [General Setup](../setup/general-setup.md)
- [Status Codes](../case-management/status-codes.md)
