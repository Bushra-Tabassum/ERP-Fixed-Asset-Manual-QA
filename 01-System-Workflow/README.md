# Fixed Asset Management – System Workflow

## Overview

This document explains the main operational workflow of the Fixed Asset Management module used as the basis for functional and end-to-end QA testing.

The workflow represents the lifecycle of an asset from its initial creation through activation, depreciation, amendment, and eventual disposal.

---

## Main Asset Lifecycle

The primary workflow is:

**Create Draft → Finalize Asset → Create Unique ID → Localize → Start Operation → Create Depreciation → Start Depreciation**

### 1. Create Draft

The asset record is initially created in draft status.

At this stage, users enter the basic asset information required to begin the asset lifecycle.

### 2. Finalize Asset

The draft asset is reviewed and finalized.

After finalization, the asset becomes available for subsequent asset management operations.

### 3. Create Unique ID

A unique identifier is generated for the finalized asset.

This allows the asset to be uniquely tracked throughout the system.

### 4. Localize

The asset is assigned to its operational location or organizational unit.

Examples may include a branch, department, cost center, or physical location depending on system configuration.

### 5. Start Operation

The asset is placed into operational use.

This represents the point at which the asset becomes active within the organization.

### 6. Create Depreciation

Depreciation-related information is configured for the asset.

This may include the depreciation method, useful life, salvage value, depreciation frequency, and other accounting parameters.

### 7. Start Depreciation

Depreciation processing begins according to the configured depreciation settings.

Once depreciation has started, additional lifecycle operations may become available.

---

## Operations After Depreciation Starts

After depreciation begins, the asset may follow additional operational paths.

### Amendment

Asset information may be amended when approved changes are required.

The availability and effect of amendment depend on the asset's current lifecycle state and applicable business rules.

### Pause / Resume

Depreciation may be temporarily paused.

When the asset becomes eligible again, depreciation can be resumed and continue according to the configured rules.

### Dispose

The asset may eventually be removed from active service.

Disposal may involve sale, scrap, retirement, or another supported disposal method.

---

## QA Purpose

This workflow was used as the foundation for:

- Functional testing
- End-to-end workflow testing
- Business rule validation
- Positive and negative testing
- State transition testing
- Permission testing
- Integration testing
- Depreciation and accounting validation
- Regression testing

Test scenarios and test cases in this repository are mapped to different stages of this workflow.

---

## Workflow Diagram

![Fixed Asset Management Workflow](./fixed-asset-workflow.png)

---

> All workflow information shown in this portfolio has been sanitized and simplified. No confidential company or client information is included.
