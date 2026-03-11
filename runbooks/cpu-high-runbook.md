# Incident Runbook: High CPU Usage

## Detection
High CPU utilization can be detected via the Grafana dashboard when the CPU panel exceeds normal thresholds.

## Investigation Steps
1. Open the Grafana dashboard.
2. Identify spikes in the **Host CPU Utilization** panel.
3. Check the time range of the spike.
4. Verify running processes on the host using:
   - `top`
   - `htop`
   - `docker stats`

## Possible Causes
- Resource intensive applications
- Traffic spikes
- Misconfigured services
- Infinite loops or runaway processes

## Resolution
- Restart affected services
- Limit CPU usage via container settings
- Scale the application if necessary

## Post-Incident
Document the root cause and update monitoring thresholds if required.