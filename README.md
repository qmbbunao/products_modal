HTML CODE:
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Checkout — Collectibles</title>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"/>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css"/>
  <link rel="stylesheet" href="style.css"/>
</head>
<body>

  

  <!-- ── Checkout Page ───────────────────────────────────── -->
  <main class="py-5" id="checkoutPage">
    <div class="container">
      <h1 class="page-title mb-4">Checkout</h1>
      <div class="row g-4 align-items-start">

        <!-- LEFT -->
        <div class="col-lg-7">

          <!-- 01 Contact -->
          <section class="checkout-section mb-3">
            <div class="section-label">
              <span class="section-num">01</span>
              <h2 class="section-title">Contact Information</h2>
            </div>
            <div class="section-body">
              <div class="row g-3">
                <div class="col-sm-6">
                  <div class="field-label">First Name</div>
                  <div class="field-box">Juan</div>
                </div>
                <div class="col-sm-6">
                  <div class="field-label">Last Name</div>
                  <div class="field-box">dela Cruz</div>
                </div>
                <div class="col-12">
                  <div class="field-label">Email Address</div>
                  <div class="field-box">juan@email.com</div>
                </div>
                <div class="col-12">
                  <div class="field-label">Phone Number</div>
                  <div class="field-box">🇵🇭 +63 917 123 4567</div>
                </div>
              </div>
            </div>
          </section>

          <!-- 02 Shipping -->
          <section class="checkout-section mb-3">
            <div class="section-label">
              <span class="section-num">02</span>
              <h2 class="section-title">Shipping Address</h2>
            </div>
            <div class="section-body">
              <div class="row g-3">
                <div class="col-12">
                  <div class="field-label">Street Address / Barangay</div>
                  <div class="field-box">123 Rizal St., Brgy. Bagong Barrio</div>
                </div>
                <div class="col-sm-6">
                  <div class="field-label">City / Municipality</div>
                  <div class="field-box">Caloocan City</div>
                </div>
                <div class="col-sm-6">
                  <div class="field-label">Province</div>
                  <div class="field-box">Metro Manila (NCR)</div>
                </div>
                <div class="col-sm-6">
                  <div class="field-label">ZIP Code</div>
                  <div class="field-box">1400</div>
                </div>
                <div class="col-sm-6">
                  <div class="field-label">Country</div>
                  <div class="field-box field-box--muted">Philippines</div>
                </div>
                <div class="col-12">
                  <div class="field-label">Delivery Notes</div>
                  <div class="field-box field-box--muted">Leave at the gate, call upon arrival.</div>
                </div>
              </div>
            </div>
          </section>

          <!-- 03 Payment -->
          <section class="checkout-section mb-3">
            <div class="section-label">
              <span class="section-num">03</span>
              <h2 class="section-title">Payment Method</h2>
            </div>
            <div class="section-body">

              <!-- Tabs -->
              <div class="d-flex gap-2 mb-4 flex-wrap" id="paymentTabs">
                <button class="pay-tab active" data-target="panel-card">
                  <i class="bi bi-credit-card-2-front"></i> Credit / Debit Card
                </button>
                <button class="pay-tab" data-target="panel-gcash">
                  <i class="bi bi-phone"></i> GCash
                </button>
                <button class="pay-tab" data-target="panel-cod">
                  <i class="bi bi-cash-coin"></i> Cash on Delivery
                </button>
              </div>

              <!-- Card -->
              <div class="pay-panel" id="panel-card">
                <div class="row g-3">
                  <div class="col-12">
                    <div class="field-label">Cardholder Name</div>
                    <div class="field-box">Juan dela Cruz</div>
                  </div>
                  <div class="col-12">
                    <div class="field-label">Card Number</div>
                    <div class="field-box d-flex align-items-center justify-content-between">
                      <span>•••• •••• •••• 4242</span>
                      <i class="bi bi-credit-card-2-front-fill" style="color:#2563eb;font-size:1.1rem;"></i>
                    </div>
                  </div>
                  <div class="col-sm-6">
                    <div class="field-label">Expiry Date</div>
                    <div class="field-box">08 / 27</div>
                  </div>
                  <div class="col-sm-6">
                    <div class="field-label">CVV</div>
                    <div class="field-box">•••</div>
                  </div>
                </div>
              </div>

              <!-- GCash -->
              <div class="pay-panel d-none" id="panel-gcash">
                <div class="gcash-box p-4">
                  <div class="d-flex align-items-center gap-3 mb-4">
                    <div class="gcash-logo">G</div>
                    <div>
                      <div class="fw-semibold">GCash</div>
                      <div class="text-muted small">Mobile wallet payment</div>
                    </div>
                  </div>

                  <div class="field-label">Registered GCash Number</div>
                  <div class="field-box mb-3">🇵🇭 +63 917 123 4567</div>

                  <!-- OTP section (hidden until Send OTP clicked) -->
                  <div id="gcashOtpSection" class="d-none">
                    <div class="field-label">Enter OTP</div>
                    <div class="otp-inputs d-flex gap-2 mb-2">
                      <input type="text" class="otp-box form-control text-center" maxlength="1" id="otp1"/>
                      <input type="text" class="otp-box form-control text-center" maxlength="1" id="otp2"/>
                      <input type="text" class="otp-box form-control text-center" maxlength="1" id="otp3"/>
                      <input type="text" class="otp-box form-control text-center" maxlength="1" id="otp4"/>
                      <input type="text" class="otp-box form-control text-center" maxlength="1" id="otp5"/>
                      <input type="text" class="otp-box form-control text-center" maxlength="1" id="otp6"/>
                    </div>
                    <div id="otpMsg" class="small mb-3 d-none"></div>
                    <div class="text-muted small mb-3">OTP sent to +63 917 123 4567. <a href="#" id="resendOtp" class="text-primary">Resend</a></div>
                    <button class="btn btn-gcash-verify w-100" id="verifyOtpBtn">
                      <span class="btn-text">Verify OTP</span>
                      <span class="btn-loading d-none"><span class="spinner-border spinner-border-sm me-2"></span>Verifying…</span>
                    </button>
                  </div>

                  <div id="gcashVerified" class="d-none">
                    <div class="verified-badge"><i class="bi bi-check-circle-fill me-2"></i>GCash number verified!</div>
                  </div>

                  <button class="btn btn-gcash-send w-100" id="sendOtpBtn">
                    <i class="bi bi-send me-2"></i>Send OTP
                  </button>
                </div>
              </div>

              <!-- COD -->
              <div class="pay-panel d-none" id="panel-cod">
                <div class="cod-box p-4">
                  <div class="d-flex align-items-start gap-3 mb-4">
                    <div class="cod-icon"><i class="bi bi-cash-stack"></i></div>
                    <div>
                      <p class="mb-1 fw-semibold">Cash on Delivery</p>
                      <p class="text-muted small mb-0">Pay in cash when your order arrives at your doorstep.</p>
                    </div>
                  </div>

                  <div class="cod-amount-box mb-3">
                    <div class="d-flex justify-content-between align-items-center">
                      <span class="text-muted small">Amount to prepare</span>
                      <span class="fw-bold fs-5" id="codAmountDisplay">₱2,598.00</span>
                    </div>
                  </div>

                  <ul class="cod-notes list-unstyled mb-4">
                    <li><i class="bi bi-info-circle text-warning me-2"></i>Please prepare the <strong>exact amount</strong>.</li>
                    <li><i class="bi bi-info-circle text-warning me-2"></i>Our courier may not carry change.</li>
                    <li><i class="bi bi-info-circle text-warning me-2"></i>Have a valid ID ready for verification.</li>
                  </ul>

                  <div id="codAgreementRow" class="d-flex align-items-start gap-2">
                    <input class="form-check-input mt-1 flex-shrink-0" type="checkbox" id="codAgree"/>
                    <label class="form-check-label small" for="codAgree">
                      I understand and agree to the Cash on Delivery terms above.
                    </label>
                  </div>
                  <div id="codAgreedBadge" class="d-none">
                    <div class="verified-badge"><i class="bi bi-check-circle-fill me-2"></i>COD terms accepted!</div>
                  </div>
                </div>
              </div>

            </div>
          </section>
        </div>

        <!-- RIGHT: Summary -->
        <div class="col-lg-5">
          <div class="summary-card sticky-top">

            <div class="summary-header">
              <h2 class="summary-title">Order Summary</h2>
            </div>

            <div class="summary-items">
              <div class="summary-item d-flex align-items-center gap-3">
                <div class="item-img-wrap">
                  <img src="https://placehold.co/60x60/eef2ff/4f46e5?text=11" alt="Eleven" class="item-img"/>
                  <span class="item-qty-badge">1</span>
                </div>
                <div class="flex-grow-1">
                  <p class="item-name mb-0">Funko Pop – Stranger Things</p>
                  <p class="item-variant mb-0">Eleven</p>
                </div>
                <p class="item-price mb-0">₱1,299.00</p>
              </div>
              <div class="summary-item d-flex align-items-center gap-3">
                <div class="item-img-wrap">
                  <img src="https://placehold.co/60x60/eef2ff/4f46e5?text=W" alt="Will" class="item-img"/>
                  <span class="item-qty-badge">1</span>
                </div>
                <div class="flex-grow-1">
                  <p class="item-name mb-0">Funko Pop – Stranger Things</p>
                  <p class="item-variant mb-0">Will</p>
                </div>
                <p class="item-price mb-0">₱1,299.00</p>
              </div>
            </div>

            
            <div class="summary-totals px-4 pb-3">
              <div class="d-flex justify-content-between mb-2">
                <span class="text-muted">Subtotal</span><span>₱2,598.00</span>
              </div>
              <div class="d-flex justify-content-between mb-2">
                <span class="text-muted">Shipping</span>
                <span class="text-success fw-semibold">Free</span>
              </div>
              <div class="d-flex justify-content-between mb-2 d-none" id="discountRow">
                <span class="text-muted">Discount</span>
                <span class="text-danger" id="discountAmt">–₱0.00</span>
              </div>
              <hr class="summary-divider"/>
              <div class="d-flex justify-content-between total-row">
                <span>Total</span><span id="totalAmt">₱2,598.00</span>
              </div>
            </div>

            <div class="px-4 pb-4">
              <button class="btn btn-place w-100" id="placeOrderBtn">
                Place Order <i class="bi bi-arrow-right ms-1"></i>
              </button>
              <p class="secure-note text-center mt-3 mb-0">
                <i class="bi bi-shield-lock-fill me-1"></i> Secured checkout · SSL encrypted
              </p>
            </div>

          </div>
        </div>

      </div>
    </div>
  </main>

  <!-- ── Order Success Page (hidden) ────────────────────── -->
  <div id="successPage" class="d-none">
    <div class="success-page">
      <div class="container">
        <div class="success-card mx-auto">

          <!-- Animated check -->
          <div class="success-anim mb-4">
            <div class="success-circle">
              <i class="bi bi-check-lg"></i>
            </div>
          </div>

          <h2 class="success-title">Order Confirmed!</h2>
          <p class="success-sub">Thank you, <strong>Juan</strong>! Your order has been placed successfully.</p>

          <!-- Order details box -->
          <div class="success-details">
            <div class="success-detail-row">
              <span class="sd-label">Order Number</span>
              <span class="sd-value fw-semibold" id="successOrderNum">#COL-00000</span>
            </div>
            <div class="success-detail-row">
              <span class="sd-label">Payment Method</span>
              <span class="sd-value" id="successPayment">Credit / Debit Card</span>
            </div>
            <div class="success-detail-row">
              <span class="sd-label">Total Paid</span>
              <span class="sd-value fw-semibold" id="successTotal">₱2,598.00</span>
            </div>
            <div class="success-detail-row">
              <span class="sd-label">Estimated Delivery</span>
              <span class="sd-value" id="successDelivery">—</span>
            </div>
            <div class="success-detail-row border-0 pb-0">
              <span class="sd-label">Deliver to</span>
              <span class="sd-value">123 Rizal St., Caloocan City, 1400</span>
            </div>
          </div>

          <!-- Items recap -->
          <div class="success-items mt-4">
            <div class="d-flex align-items-center gap-3 pb-3" style="border-bottom:1px solid #f3f4f6;">
              <img src="https://placehold.co/48x48/eef2ff/4f46e5?text=11" class="rounded-2" style="width:48px;height:48px;border:1px solid #e5e7eb;"/>
              <div class="flex-grow-1">
                <div class="fw-semibold" style="font-size:.88rem;">Funko Pop – Stranger Things · Eleven</div>
                <div class="text-muted" style="font-size:.78rem;">Qty: 1</div>
              </div>
              <div class="fw-semibold" style="font-size:.88rem;">₱1,299.00</div>
            </div>
            <div class="d-flex align-items-center gap-3 pt-3">
              <img src="https://placehold.co/48x48/eef2ff/4f46e5?text=W" class="rounded-2" style="width:48px;height:48px;border:1px solid #e5e7eb;"/>
              <div class="flex-grow-1">
                <div class="fw-semibold" style="font-size:.88rem;">Funko Pop – Stranger Things · Will</div>
                <div class="text-muted" style="font-size:.78rem;">Qty: 1</div>
              </div>
              <div class="fw-semibold" style="font-size:.88rem;">₱1,299.00</div>
            </div>
          </div>

          <p class="success-email-note mt-4">
            <i class="bi bi-envelope-fill me-2 text-primary"></i>A confirmation has been sent to <strong>juan@email.com</strong>
          </p>

          <div class="d-flex gap-3 justify-content-center mt-4 flex-wrap">
  <a href="#" class="btn btn-place px-4">Continue Shopping</a>
</div>

        </div>
      </div>
    </div>
  </div>

  <!-- ── Confirm Order Modal ─────────────────────────────── -->
  <div class="modal fade" id="confirmModal" tabindex="-1" aria-hidden="true">
    <div class="modal-dialog modal-dialog-centered">
      <div class="modal-content confirm-modal-content">
        <div class="modal-header border-0 pb-0">
          <h5 class="modal-title fw-bold">Confirm Your Order</h5>
          <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
        </div>
        <div class="modal-body pt-3">

          <!-- Mini recap -->
          <div class="confirm-recap mb-3">
            <div class="d-flex justify-content-between small mb-1">
              <span class="text-muted">Items (2)</span><span>₱2,598.00</span>
            </div>
            <div class="d-flex justify-content-between small mb-1">
              <span class="text-muted">Shipping</span><span class="text-success">Free</span>
            </div>
            <div class="d-flex justify-content-between small mb-1 d-none" id="confirmDiscountRow">
              <span class="text-muted">Discount</span><span class="text-danger" id="confirmDiscountAmt"></span>
            </div>
            <hr class="my-2"/>
            <div class="d-flex justify-content-between fw-bold">
              <span>Total</span><span id="confirmTotal">₱2,598.00</span>
            </div>
          </div>

          <div class="confirm-method-box mb-1">
            <i class="bi bi-credit-card me-2 text-primary"></i>
            <span id="confirmPaymentLabel">Credit / Debit Card</span>
          </div>
          <div class="confirm-address-box">
            <i class="bi bi-geo-alt me-2 text-danger"></i>
            123 Rizal St., Brgy. Bagong Barrio, Caloocan City, 1400
          </div>

        </div>
        <div class="modal-footer border-0 pt-0">
          <button type="button" class="btn btn-outline-secondary rounded-3 px-4" data-bs-dismiss="modal">Go Back</button>
          <button type="button" class="btn btn-place px-4" id="confirmOrderBtn">
            <span class="btn-text">Confirm &amp; Pay</span>
            <span class="btn-loading d-none"><span class="spinner-border spinner-border-sm me-2"></span>Placing…</span>
          </button>
        </div>
      </div>
    </div>
  </div>

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
  <script src="checkout.js"></script>
</body>
</html>
-------------------------------------------------------------------------------------------------------------------------------
CSS CODE:
/* ============================================================
   checkout.css
   ============================================================ */

:root {
  --brand:      #2563eb;
  --brand-dark: #1d4ed8;
  --bg:         #f3f4f6;
  --surface:    #ffffff;
  --border:     #e5e7eb;
  --text:       #111827;
  --muted:      #6b7280;
  --success:    #16a34a;
  --warning:    #d97706;
  --radius:     10px;
  --shadow:     0 2px 16px rgba(0,0,0,.07);
}

* { box-sizing: border-box; }

body {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
  background: var(--bg);
  color: var(--text);
  font-size: 15px;
  line-height: 1.6;
}



/* ── Page title ──────────────────────────────────────────── */
.page-title { font-size: 1.75rem; font-weight: 700; letter-spacing: -.4px; }

/* ── Checkout Section ────────────────────────────────────── */
.checkout-section {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  overflow: hidden;
}
.section-label {
  display: flex; align-items: center; gap: 12px;
  padding: 16px 22px;
  border-bottom: 1px solid var(--border);
  background: #f9fafb;
}
.section-num {
  font-size: .72rem; font-weight: 700; color: var(--brand);
  background: #eff6ff; border: 1px solid #bfdbfe;
  border-radius: 6px; padding: 2px 8px; letter-spacing: .5px;
}
.section-title { font-size: .95rem; font-weight: 600; margin: 0; }
.section-body  { padding: 20px 22px; }

/* ── Field boxes ─────────────────────────────────────────── */
.field-label {
  font-size: .72rem; font-weight: 600; color: var(--muted);
  text-transform: uppercase; letter-spacing: .5px; margin-bottom: 5px;
}
.field-box {
  background: #f9fafb; border: 1px solid var(--border);
  border-radius: 8px; padding: 10px 13px;
  font-size: .9rem; color: var(--text); min-height: 42px;
}
.field-box--muted { color: var(--muted); }

/* ── Payment Tabs ────────────────────────────────────────── */
.pay-tab {
  background: #f9fafb; border: 1px solid var(--border);
  border-radius: 8px; padding: 8px 14px;
  font-size: .83rem; font-weight: 500; cursor: pointer;
  color: var(--muted); display: inline-flex; align-items: center; gap: 6px;
  transition: all .15s;
}
.pay-tab:hover  { border-color: var(--brand); color: var(--brand); }
.pay-tab.active { background: var(--brand); border-color: var(--brand); color: #fff; }

/* ── GCash Panel ─────────────────────────────────────────── */
.gcash-box {
  background: #f0f6ff; border: 1px solid #bfdbfe;
  border-radius: 10px;
}
.gcash-logo {
  width: 44px; height: 44px; border-radius: 10px;
  background: #007bff; color: #fff;
  font-weight: 800; font-size: 1.4rem;
  display: flex; align-items: center; justify-content: center;
  flex-shrink: 0;
}

/* OTP boxes */
.otp-box {
  width: 46px !important; height: 52px;
  font-size: 1.3rem; font-weight: 700;
  border: 1.5px solid var(--border); border-radius: 8px;
  padding: 0; text-align: center;
  transition: border-color .15s, box-shadow .15s;
}
.otp-box:focus {
  border-color: var(--brand);
  box-shadow: 0 0 0 3px rgba(37,99,235,.15);
  outline: none;
}
.otp-box.otp-filled { border-color: var(--brand); background: #eff6ff; }

.btn-gcash-send {
  background: #007bff; color: #fff;
  border: none; border-radius: 8px;
  font-weight: 600; font-size: .88rem;
  padding: 10px; transition: background .15s;
}
.btn-gcash-send:hover { background: #0056d3; color: #fff; }

.btn-gcash-verify {
  background: var(--brand); color: #fff;
  border: none; border-radius: 8px;
  font-weight: 600; font-size: .88rem;
  padding: 10px; transition: background .15s;
}
.btn-gcash-verify:hover { background: var(--brand-dark); color: #fff; }

.verified-badge {
  background: #f0fdf4; border: 1px solid #86efac;
  border-radius: 8px; padding: 10px 14px;
  color: var(--success); font-weight: 600; font-size: .88rem;
  margin-bottom: 12px;
}

/* ── COD Panel ───────────────────────────────────────────── */
.cod-box {
  background: #fffbeb; border: 1px solid #fde68a;
  border-radius: 10px;
}
.cod-icon {
  width: 48px; height: 48px; border-radius: 10px;
  background: var(--success); color: #fff;
  font-size: 1.3rem; display: flex;
  align-items: center; justify-content: center; flex-shrink: 0;
}
.cod-amount-box {
  background: #fff; border: 1px solid #fde68a;
  border-radius: 8px; padding: 12px 14px;
}
.cod-notes li {
  font-size: .85rem; color: #374151; margin-bottom: 6px;
}
.form-check-input:checked { background-color: var(--success); border-color: var(--success); }

/* ── Summary Card ────────────────────────────────────────── */
.summary-card {
  background: var(--surface); border: 1px solid var(--border);
  border-radius: var(--radius); box-shadow: var(--shadow);
  top: 80px; overflow: hidden;
}
.summary-header {
  padding: 16px 22px; border-bottom: 1px solid var(--border);
  background: #f9fafb;
}
.summary-title { font-size: .95rem; font-weight: 600; margin: 0; }

.summary-items {
  padding: 14px 22px; border-bottom: 1px solid var(--border);
  display: flex; flex-direction: column; gap: 14px;
}
.summary-item {
  padding-bottom: 14px; border-bottom: 1px solid #f3f4f6;
}
.summary-item:last-child { border-bottom: none; padding-bottom: 0; }
.item-img-wrap { position: relative; flex-shrink: 0; }
.item-img {
  width: 56px; height: 56px; border-radius: 8px;
  object-fit: cover; border: 1px solid var(--border);
}
.item-qty-badge {
  position: absolute; top: -6px; right: -6px;
  background: var(--brand); color: #fff;
  font-size: .6rem; font-weight: 700;
  width: 18px; height: 18px; border-radius: 50%;
  display: flex; align-items: center; justify-content: center;
  border: 2px solid var(--surface);
}
.item-name    { font-size: .85rem; font-weight: 600; }
.item-variant { font-size: .78rem; color: var(--muted); }
.item-price   { font-size: .88rem; font-weight: 700; white-space: nowrap; }

/* ── Coupon ──────────────────────────────────────────────── */
.coupon-row { border-bottom: 1px solid var(--border); }
.coupon-input {
  border: 1px solid var(--border); border-right: none;
  border-radius: 8px 0 0 8px; font-size: .85rem; padding: 9px 13px;
}
.coupon-input:focus { border-color: var(--brand); box-shadow: none; outline: none; }
.coupon-btn {
  border: 1px solid var(--border); border-left: none;
  border-radius: 0 8px 8px 0; font-size: .83rem; font-weight: 600;
  padding: 9px 16px; color: var(--brand); background: #eff6ff;
  transition: all .15s;
}
.coupon-btn:hover { background: var(--brand); color: #fff; border-color: var(--brand); }

/* ── Totals ──────────────────────────────────────────────── */
.summary-totals { padding-top: 14px; }
.summary-divider { border-color: var(--border); margin: 12px 0; }
.total-row { font-size: 1.05rem; font-weight: 700; }

/* ── Place Order Button ──────────────────────────────────── */
.btn-place {
  background: var(--brand); color: #fff;
  font-weight: 600; font-size: .95rem;
  padding: 12px 20px; border-radius: 9px; border: none;
  transition: background .15s, transform .1s;
  box-shadow: 0 3px 12px rgba(37,99,235,.25);
}
.btn-place:hover  { background: var(--brand-dark); color: #fff; transform: translateY(-1px); }
.btn-place:active { transform: translateY(0); }

.secure-note { font-size: .75rem; color: var(--muted); }

/* ── Confirm Modal ───────────────────────────────────────── */
.confirm-modal-content { border: none; border-radius: 14px; }
.confirm-recap {
  background: #f9fafb; border: 1px solid var(--border);
  border-radius: 9px; padding: 14px;
}
.confirm-method-box,
.confirm-address-box {
  background: #f9fafb; border: 1px solid var(--border);
  border-radius: 8px; padding: 10px 13px;
  font-size: .85rem; margin-bottom: 8px;
}

/* ── Success Page ────────────────────────────────────────── */
.success-page {
  min-height: 100vh; background: var(--bg);
  display: flex; align-items: flex-start;
  padding: 60px 0;
}
.success-card {
  background: var(--surface); border: 1px solid var(--border);
  border-radius: 16px; padding: 48px 40px;
  max-width: 560px; width: 100%;
  box-shadow: 0 4px 32px rgba(0,0,0,.08);
  text-align: center;
}

/* Animated success circle */
.success-anim { display: flex; justify-content: center; }
.success-circle {
  width: 80px; height: 80px; border-radius: 50%;
  background: var(--success); color: #fff;
  font-size: 2.2rem; display: flex;
  align-items: center; justify-content: center;
  animation: popIn .5s cubic-bezier(.175,.885,.32,1.275) both;
  box-shadow: 0 6px 24px rgba(22,163,74,.3);
}
@keyframes popIn {
  from { transform: scale(0); opacity: 0; }
  to   { transform: scale(1); opacity: 1; }
}

.success-title { font-size: 1.6rem; font-weight: 700; letter-spacing: -.4px; margin-bottom: 6px; }
.success-sub   { color: var(--muted); font-size: .95rem; margin-bottom: 0; }

.success-details {
  background: #f9fafb; border: 1px solid var(--border);
  border-radius: 10px; overflow: hidden;
  text-align: left; margin-top: 24px;
}
.success-detail-row {
  display: flex; justify-content: space-between; align-items: center;
  padding: 11px 16px; border-bottom: 1px solid var(--border);
  font-size: .88rem;
}
.sd-label { color: var(--muted); }
.sd-value  { color: var(--text); }

.success-items {
  background: #f9fafb; border: 1px solid var(--border);
  border-radius: 10px; padding: 14px 16px;
  text-align: left;
}
.success-email-note {
  font-size: .83rem; color: var(--muted); margin-bottom: 0;
}

/* ── Responsive ──────────────────────────────────────────── */
@media (max-width: 767px) {
  .section-body, .section-label { padding-left: 16px; padding-right: 16px; }
  .summary-items, .summary-totals, .coupon-row, .px-4 {
    padding-left: 16px !important; padding-right: 16px !important;
  }
  .pb-4 { padding-bottom: 16px !important; }
  .success-card { padding: 32px 20px; }
  .otp-box { width: 40px !important; height: 46px; font-size: 1.1rem; }
}
.header-steps {
  display: none !important;
}
----------------------------------------------------------------------------------------------------
JS CODE:
/* ============================================================
   checkout.js (CLEAN VERSION – no promo / no discount)
   ============================================================ */

document.addEventListener('DOMContentLoaded', () => {

  const SUBTOTAL = 2598;
  let totalAmount = SUBTOTAL;
  let activePaymentMethod = 'Credit / Debit Card';

  /* ── Helpers ───────────────────────────────────────────── */
  function formatPHP(n) {
    return '₱' + n.toLocaleString('en-PH', { minimumFractionDigits: 2 });
  }

  function randomOrderNum() {
    return '#COL-' + Math.floor(10000 + Math.random() * 90000);
  }

  function deliveryDate() {
    const d = new Date();
    d.setDate(d.getDate() + Math.floor(3 + Math.random() * 3)); // 3–5 days
    return d.toLocaleDateString('en-PH', {
      weekday: 'long',
      month: 'long',
      day: 'numeric'
    });
  }

  /* ── Payment Tab Switcher ──────────────────────────────── */
  const payTabs   = document.querySelectorAll('.pay-tab');
  const payPanels = document.querySelectorAll('.pay-panel');

  payTabs.forEach(tab => {
    tab.addEventListener('click', () => {
      payTabs.forEach(t => t.classList.remove('active'));
      payPanels.forEach(p => p.classList.add('d-none'));

      tab.classList.add('active');
      document.getElementById(tab.dataset.target)?.classList.remove('d-none');

      const map = {
        'panel-card':  'Credit / Debit Card',
        'panel-gcash': 'GCash',
        'panel-cod':   'Cash on Delivery',
      };

      activePaymentMethod = map[tab.dataset.target] || 'Credit / Debit Card';
    });
  });

  /* ── GCash OTP Flow ────────────────────────────────────── */
  const sendOtpBtn      = document.getElementById('sendOtpBtn');
  const gcashOtpSection = document.getElementById('gcashOtpSection');
  const gcashVerified   = document.getElementById('gcashVerified');
  const verifyOtpBtn    = document.getElementById('verifyOtpBtn');
  const otpMsg          = document.getElementById('otpMsg');
  const resendOtp       = document.getElementById('resendOtp');
  const otpBoxes        = document.querySelectorAll('.otp-box');

  otpBoxes.forEach((box, i) => {
    box.addEventListener('input', () => {
      box.value = box.value.replace(/\D/, '');

      if (box.value) {
        box.classList.add('otp-filled');
        if (i < otpBoxes.length - 1) otpBoxes[i + 1].focus();
      } else {
        box.classList.remove('otp-filled');
      }
    });

    box.addEventListener('keydown', e => {
      if (e.key === 'Backspace' && !box.value && i > 0) {
        otpBoxes[i - 1].focus();
      }
    });
  });

  sendOtpBtn?.addEventListener('click', () => {
    sendOtpBtn.innerHTML = '<span class="spinner-border spinner-border-sm me-2"></span>Sending…';
    sendOtpBtn.disabled = true;

    setTimeout(() => {
      sendOtpBtn.classList.add('d-none');
      gcashOtpSection.classList.remove('d-none');
      otpBoxes[0].focus();
    }, 1200);
  });

  resendOtp?.addEventListener('click', e => {
    e.preventDefault();

    otpBoxes.forEach(b => {
      b.value = '';
      b.classList.remove('otp-filled');
    });

    otpMsg.classList.add('d-none');
    resendOtp.textContent = 'Sent!';

    setTimeout(() => resendOtp.textContent = 'Resend', 2500);

    otpBoxes[0].focus();
  });

  verifyOtpBtn?.addEventListener('click', () => {
    const code = [...otpBoxes].map(b => b.value).join('');
    otpMsg.classList.remove('d-none', 'text-success', 'text-danger');

    if (code.length < 6) {
      otpMsg.textContent = 'Please enter the complete 6-digit OTP.';
      otpMsg.className = 'small mb-3 text-danger';
      return;
    }

    verifyOtpBtn.querySelector('.btn-text').classList.add('d-none');
    verifyOtpBtn.querySelector('.btn-loading').classList.remove('d-none');
    verifyOtpBtn.disabled = true;

    setTimeout(() => {
      gcashOtpSection.classList.add('d-none');
      gcashVerified.classList.remove('d-none');
    }, 1400);
  });

  /* ── COD Checkbox ──────────────────────────────────────── */
  const codAgree        = document.getElementById('codAgree');
  const codAgreedBadge  = document.getElementById('codAgreedBadge');
  const codAgreementRow = document.getElementById('codAgreementRow');

  codAgree?.addEventListener('change', () => {
    if (codAgree.checked) {
      setTimeout(() => {
        codAgreementRow.classList.add('d-none');
        codAgreedBadge.classList.remove('d-none');
      }, 300);
    } else {
      codAgreementRow.classList.remove('d-none');
      codAgreedBadge.classList.add('d-none');
    }
  });

  /* ── Place Order → Confirm Modal ───────────────────────── */
  const placeOrderBtn   = document.getElementById('placeOrderBtn');
  const confirmModal    = new bootstrap.Modal(document.getElementById('confirmModal'));
  const confirmTotal    = document.getElementById('confirmTotal');
  const confirmPayLabel = document.getElementById('confirmPaymentLabel');

  placeOrderBtn?.addEventListener('click', () => {
    confirmTotal.textContent    = formatPHP(totalAmount);
    confirmPayLabel.textContent = activePaymentMethod;
    confirmModal.show();
  });

  /* ── Confirm & Pay → Success Page ──────────────────────── */
  const confirmOrderBtn  = document.getElementById('confirmOrderBtn');
  const checkoutPage     = document.getElementById('checkoutPage');
  const successPage      = document.getElementById('successPage');
  const stepCheckout     = document.getElementById('stepCheckout');
  const stepConfirmation = document.getElementById('stepConfirmation');

  confirmOrderBtn?.addEventListener('click', () => {
    const btnText    = confirmOrderBtn.querySelector('.btn-text');
    const btnLoading = confirmOrderBtn.querySelector('.btn-loading');

    btnText.classList.add('d-none');
    btnLoading.classList.remove('d-none');
    confirmOrderBtn.disabled = true;

    setTimeout(() => {
      confirmModal.hide();

      // Populate success page
      document.getElementById('successOrderNum').textContent = randomOrderNum();
      document.getElementById('successPayment').textContent  = activePaymentMethod;
      document.getElementById('successTotal').textContent    = formatPHP(totalAmount);
      document.getElementById('successDelivery').textContent = deliveryDate();

      // Switch UI
      checkoutPage.classList.add('d-none');
      successPage.classList.remove('d-none');

      

      window.scrollTo({ top: 0, behavior: 'smooth' });
    }, 1800);
  });

});

