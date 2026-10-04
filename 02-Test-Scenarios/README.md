# Fixed Asset Management – Test Scenarios

## 1. Asset Creation

- Verify a new asset can be created with valid mandatory data.
- Verify required fields are properly validated.
- Verify invalid numeric, date, and text inputs are rejected.
- Verify duplicate or conflicting asset information is handled correctly.
- Verify the asset remains in Draft status after successful creation.
- Verify Reset/Clear behavior works correctly before saving.
- Verify field-level validations remain consistent during update/edit.

---

## 2. Asset Finalization

- Verify a valid Draft asset can be finalized successfully.
- Verify finalization is blocked when mandatory data is incomplete.
- Verify accounting information is validated before finalization.
- Verify the asset status changes correctly after finalization.
- Verify unauthorized users cannot finalize assets.
- Verify editable fields behave correctly before and after finalization.

---

## 3. Unique ID Creation

- Verify a unique asset ID can be created for a finalized asset.
- Verify duplicate IDs cannot be generated.
- Verify the generated ID is linked to the correct asset.
- Verify the ID remains unchanged after later lifecycle operations.

---

## 4. Localization

- Verify an asset can be assigned to a valid location.
- Verify required location information is validated.
- Verify invalid or inactive locations cannot be assigned.
- Verify localization data is retained correctly after saving.

---

## 5. Start Operation

- Verify a localized asset can be moved into operational status.
- Verify operation cannot start when prerequisites are incomplete.
- Verify operation date validations are enforced.
- Verify relevant accounting transactions are generated correctly.
- Verify the asset status changes correctly after starting operation.

---

## 6. Depreciation Setup

- Verify depreciation can be configured using valid parameters.
- Verify depreciation method selection works correctly.
- Verify useful life, salvage value, and frequency validations.
- Verify unsupported numeric formats or invalid values are rejected.
- Verify depreciation cannot be created when mandatory configuration is missing.
- Verify calculated values match the selected depreciation method.

---

## 7. Start Depreciation

- Verify depreciation starts successfully for an eligible asset.
- Verify depreciation cannot start before operation begins.
- Verify depreciation start date rules are enforced.
- Verify monthly depreciation values are calculated correctly.
- Verify accounting debit and credit totals remain balanced.
- Verify depreciation status updates correctly.

---

## 8. Amendment

- Verify an eligible asset can be amended after depreciation starts.
- Verify restricted fields cannot be changed where applicable.
- Verify invalid amendment values are rejected.
- Verify amendment changes are reflected correctly in future processing.
- Verify amendment history/audit information is retained where applicable.

---

## 9. Pause / Resume

- Verify depreciation can be paused for an eligible asset.
- Verify no depreciation is processed while the asset is paused.
- Verify depreciation can be resumed successfully.
- Verify depreciation continues correctly after resume.
- Verify invalid pause/resume state transitions are prevented.

---

## 10. Disposal / Sale

- Verify an eligible asset can be disposed.
- Verify disposal date validations are enforced.
- Verify disposal cannot occur before required lifecycle dates.
- Verify sale proceeds are recorded correctly where applicable.
- Verify carrying value and accumulated depreciation are calculated correctly.
- Verify gain/loss on disposal is calculated correctly.
- Verify accounting entries remain balanced.
- Verify disposed assets cannot continue normal depreciation processing.

---

## 11. Role & Permission Testing

- Verify users only see actions allowed by their assigned role.
- Verify restricted actions are blocked for unauthorized users.
- Verify frontend permissions match backend authorization.
- Verify admin and non-admin behavior is consistent with requirements.

---

## 12. Integration Testing

- Verify data flows correctly between Fixed Assets and Accounting.
- Verify related transactions are reflected in the correct module.
- Verify cross-module values remain consistent.
- Verify failed integration does not leave partial or inconsistent data.
- Verify dependent workflows respond correctly to upstream changes.

---

## 13. Regression Testing

- Verify major workflows still work after changes or fixes.
- Verify previously fixed defects do not reappear.
- Verify changes to one lifecycle stage do not break later stages.
- Verify calculations remain consistent after updates.
