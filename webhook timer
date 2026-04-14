
import time
import requests
import logging

URL do webhook que será disparado
WEBHOOK_URL = "https://n8n.pontodaesfihalp.com.br/webhook/timer"

Intervalo entre cada disparo (10 minutos)
INTERVALO_SEGUNDOS = 10 * 60

Log com data e hora para acompanhar o que está acontecendo
logging.basicConfig(
    level=logging.INFO,
    format="%(asctime)s - %(message)s",
    datefmt="%Y-%m-%d %H:%M:%S"
)

def disparar_webhook():
    try:
        resposta = requests.get(WEBHOOK_URL, timeout=10)
        logging.info(f"Webhook disparado! Status: {resposta.status_code}")
    except Exception as e:
        logging.error(f"Erro ao disparar webhook: {e}")

if name == "main":
    logging.info("Iniciando timer — webhook a cada 10 minutos.")
    while True:
        disparar_webhook()
        time.sleep(INTERVALO_SEGUNDOS)
