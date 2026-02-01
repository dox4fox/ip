<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Определение IP и страны (несколько API)</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            max-width: 1000px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f5f5f5;
            color: #333;
        }
        .container {
            background-color: white;
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        h1 {
            color: #2c3e50;
            text-align: center;
            margin-bottom: 30px;
        }
        .info-box {
            background-color: #f8f9fa;
            border-radius: 5px;
            padding: 20px;
            margin-bottom: 20px;
            border-left: 4px solid #3498db;
        }
        .loading {
            text-align: center;
            margin: 20px 0;
            display: none;
        }
        .spinner {
            border: 4px solid rgba(0, 0, 0, 0.1);
            border-left-color: #3498db;
            border-radius: 50%;
            width: 30px;
            height: 30px;
            animation: spin 1s linear infinite;
            margin: 0 auto;
        }
        @keyframes spin {
            to { transform: rotate(360deg); }
        }
        .error {
            color: #e74c3c;
            text-align: center;
            margin-top: 20px;
        }
        button {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            display: block;
            margin: 20px auto;
            transition: background-color 0.3s;
        }
        button:hover {
            background-color: #2980b9;
        }
        .api-result {
            margin-top: 20px;
            padding: 15px;
            border-radius: 5px;
            background-color: #eaf7ff;
            display: none;
            margin-bottom: 15px;
        }
        .api-name {
            font-weight: bold;
            color: #2c3e50;
            margin-bottom: 10px;
            border-bottom: 1px solid #ddd;
            padding-bottom: 5px;
        }
        .ip-address {
            font-weight: bold;
            color: #2c3e50;
        }
        .country {
            font-weight: bold;
            color: #3498db;
        }
        .coordinates {
            color: #7f8c8d;
            font-size: 14px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Определение IP и страны (несколько API)</h1>

        <div class="info-box">
            <p>Для определения вашего IP-адреса и страны будут использоваться несколько публичных API. Это может занять несколько секунд.</p>
        </div>

        <div class="loading" id="loading">
            <div class="spinner"></div>
            <p>Получаю информацию...</p>
        </div>

        <button id="getDataBtn">Получить информацию</button>

        <!-- Результаты для каждого API -->
        <div class="api-result" id="result_ipapi">
            <div class="api-name">API: ip-api.com</div>
            <p>Ваш IP-адрес: <span class="ip-address" id="ipAddress_ipapi"></span></p>
            <p>Страна: <span class="country" id="country_ipapi"></span></p>
            <p>Координаты: <span class="coordinates" id="coordinates_ipapi"></span></p>
        </div>

        <div class="api-result" id="result_ipwhois">
            <div class="api-name">API: ipwhois.app</div>
            <p>Ваш IP-адрес: <span class="ip-address" id="ipAddress_ipwhois"></span></p>
            <p>Страна: <span class="country" id="country_ipwhois"></span></p>
            <p>Координаты: <span class="coordinates" id="coordinates_ipwhois"></span></p>
        </div>

        <div class="api-result" id="result_ipify">
            <div class="api-name">API: ipify + ip-api.com</div>
            <p>Ваш IP-адрес: <span class="ip-address" id="ipAddress_ipify"></span></p>
            <p>Страна: <span class="country" id="country_ipify"></span></p>
            <p>Координаты: <span class="coordinates" id="coordinates_ipify"></span></p>
        </div>

        <div class="error" id="error"></div>
    </div>

    <script>
        document.getElementById('getDataBtn').addEventListener('click', async function() {
            document.getElementById('loading').style.display = 'block';
            document.querySelectorAll('.api-result').forEach(el => el.style.display = 'none');
            document.getElementById('error').textContent = '';

            try {
                // 1. ip-api.com
                const ipapiResponse = await fetch('http://ip-api.com/json/');
                if (ipapiResponse.ok) {
                    const ipapiData = await ipapiResponse.json();
                    document.getElementById('ipAddress_ipapi').textContent = ipapiData.query;
                    document.getElementById('country_ipapi').textContent = `${ipapiData.country} (${ipapiData.countryCode})`;
                    document.getElementById('coordinates_ipapi').textContent = `${ipapiData.lat}, ${ipapiData.lon}`;
                    document.getElementById('result_ipapi').style.display = 'block';
                }

                // 2. ipwhois.app
                const ipwhoisResponse = await fetch('https://ipwhois.app/json/');
                if (ipwhoisResponse.ok) {
                    const ipwhoisData = await ipwhoisResponse.json();
                    document.getElementById('ipAddress_ipwhois').textContent = ipwhoisData.ip;
                    document.getElementById('country_ipwhois').textContent = `${ipwhoisData.country} (${ipwhoisData.country_code})`;
                    document.getElementById('coordinates_ipwhois').textContent = `${ipwhoisData.latitude}, ${ipwhoisData.longitude}`;
                    document.getElementById('result_ipwhois').style.display = 'block';
                }

                // 3. ipify + ip-api.com
                const ipifyResponse = await fetch('https://api.ipify.org?format=json');
                if (ipifyResponse.ok) {
                    const ipifyData = await ipifyResponse.json();
                    const ip = ipifyData.ip;
                    const geoResponse = await fetch(`http://ip-api.com/json/${ip}`);
                    if (geoResponse.ok) {
                        const geoData = await geoResponse.json();
                        document.getElementById('ipAddress_ipify').textContent = ip;
                        document.getElementById('country_ipify').textContent = `${geoData.country} (${geoData.countryCode})`;
                        document.getElementById('coordinates_ipify').textContent = `${geoData.lat}, ${geoData.lon}`;
                        document.getElementById('result_ipify').style.display = 'block';
                    }
                }

                document.getElementById('loading').style.display = 'none';

            } catch (error) {
                document.getElementById('error').textContent = 'Ошибка: ' + error.message;
                document.getElementById('loading').style.display = 'none';
            }
        });
    </script>
</body>
</html>
