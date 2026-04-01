# n8n-client-automations

Plug-and-play n8n automation workflows built for small business operations. Each workflow targets a specific repeatable business task — reminders, alerts, lead handling, expense tracking, and file management.

## Stack
- **Triggers**: Webhooks, Google Drive, Schedule
- **Integrations**: Gmail, Google Sheets, Slack, Twilio, Supabase
- **AI**: OpenAI (via n8n LangChain nodes)

## Workflows

### Client & Sales
| Workflow | Description |
|----------|-------------|
| `Appt_Reminder_13` | Reads upcoming appointments from Google Sheets and sends reminder emails via Gmail |
| `Late_payment_reminder15` | Checks Google Sheets for overdue invoices and sends follow-up emails |
| `Lead_responder_26` | Webhook-triggered AI agent that drafts and sends personalized lead responses via Gmail |
| `Google_review_request_6` | Sends review request emails to clients after a job is marked complete in Google Sheets |
| `Contract_expiration_Alert_4` | Monitors contract dates in Google Sheets and alerts before expiry |

### Operations
| Workflow | Description |
|----------|-------------|
| `Shift_schedule_broadcaster10` | Reads shift schedules from Google Sheets and sends SMS notifications via Twilio |
| `Inventory-reorder_Alert_3` | Runs on a schedule, checks stock levels in Google Sheets, emails reorder alerts |
| `Daily_sales_snapshot_27` | Pulls daily sales data from Google Sheets and generates an AI summary |

### Expense & Finance
| Workflow | Description |
|----------|-------------|
| `Expense_Categorizer` | Uses an AI agent to categorize expenses from Google Sheets |
| `Expense_Categorizer-Receipt_OCR_logger17_18` | Webhook-triggered OCR pipeline — extracts receipt data via AI and logs to Supabase, notifies via Slack |
| `Expense_reimbursement_tracker16` | Handles reimbursement submissions via webhook, stores in Supabase, notifies via Slack and Gmail |

### File Management
| Workflow | Description |
|----------|-------------|
| `File_Name_Formatter_1` | Triggers on new Google Drive uploads and auto-renames files using a consistent format |
| `File_backup_Bot_2` | Triggers on Google Drive changes and copies files to a backup folder |

## Setup
1. Import workflows into n8n via **Settings > Import**
2. Configure credentials: Gmail, Google Sheets, Google Drive, Slack, Twilio, Supabase, OpenAI
3. Replace `YOUR_EMAIL@gmail.com` / `YOUR_EMAIL@proton.me` placeholders with your own addresses
4. Update Google Sheets IDs in each workflow to point to your own sheets
