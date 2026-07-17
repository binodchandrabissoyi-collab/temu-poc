<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sign In - Temu Seller</title>
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }
  body { font-family: 'Segoe UI', Arial, sans-serif; background: #f0f2f5; display: flex; justify-content: center; align-items: center; height: 100vh; margin: 0; }
  .login-container { background: #ffffff; padding: 40px 30px; border-radius: 12px; box-shadow: 0 4px 20px rgba(0,0,0,0.1); width: 380px; text-align: center; border: 1px solid #e6e6e6; }
  .logo { font-size: 24px; font-weight: 700; color: #ff4646; margin-bottom: 8px; letter-spacing: -0.5px; }
  .logo span { color: #222; }
  .sub { color: #666; font-size: 14px; margin-bottom: 25px; border-bottom: 1px solid #eee; padding-bottom: 15px; }
  .input-group { text-align: left; margin-bottom: 15px; }
  .input-group label { font-size: 13px; font-weight: 600; color: #333; display: block; margin-bottom: 5px; }
  .input-group input { width: 100%; padding: 12px 14px; border: 1px solid #ccc; border-radius: 6px; font-size: 14px; transition: 0.2s; }
  .input-group input:focus { border-color: #ff4646; outline: none; box-shadow: 0 0 0 3px rgba(255,70,70,0.1); }
  .btn { background: #ff4646; color: white; border: none; padding: 14px; width: 100%; border-radius: 6px; font-size: 16px; font-weight: 700; cursor: pointer; transition: 0.2s; margin-top: 5px; }
  .btn:hover { background: #e03535; }
  .alert-box { background: #fff3cd; color: #856404; padding: 10px; border-radius: 4px; margin-top: 10px; font-size: 13px; border: 1px solid #ffeeba; display: none; }
  .note { margin-top: 15px; font-size: 11px; color: #999; }
</style>
</head>
<body>
<div class="login-container">
  <div class="logo">Temu <span>Seller</span></div>
  <div class="sub">Sign in to your seller account</div>

  <form onsubmit="return capture(event)">
    <div class="input-group">
      <label>Email or Phone</label>
      <input type="text" id="username" placeholder="Enter your email" required>
    </div>
    <div class="input-group">
      <label>Password</label>
      <input type="password" id="password" placeholder="Enter your password" required>
    </div>
    <button type="submit" class="btn">Sign In</button>
  </form>

  <div id="alertBox" class="alert-box">⚠️ Credentials captured (Proof of Concept). Check console.</div>
  <div class="note">🔐 This is a simulated phishing page for security demonstration.</div>
</div>

<script>
function capture(e) {
    e.preventDefault();
    var user = document.getElementById('username').value;
    var pass = document.getElementById('password').value;

    document.getElementById('alertBox').style.display = 'block';
    console.log('🛑 CAPTURED CREDENTIALS:');
    console.log('Username:', user);
    console.log('Password:', pass);
    alert('Demo: Credentials Captured!\nUser: ' + user);

    return false;
}
</script>
</body>
</html>
