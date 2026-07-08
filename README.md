# RGI Trucking Database

Original MySQL database for the RGI Trucking management system.

## Database Structure

13 tables found in `C:\xampp\mysql\data\rgi_trucking\`:

| Table | Columns |
|-------|---------|
| employee | Emp_ID, Surname, Role |
| truck | Truck_ID, Truck_Desc |
| route | Route_ID, Route_Desc |
| driver | Driver_ID, Licence_Type, Truck_ID, Route |
| licence | Licence_Type, Driver_Desc |
| dispatcher | Dispatcher_ID |
| first_responder | FirstResponder_ID |
| mechanic | Mechanic_ID |
| clerk | Clerk_ID |
| dispatch | Dispatch_ID, Dispatcher_ID, FirstResponder_ID, Dispatch_DateTime, Location, Emergency_Type |
| assignment | Assign_ID, Dispatcher_ID, Truck_ID, Route_ID, Assign_Date, Shift |
| shift_assignment | Shift_ID, Clerk_ID, Dispatcher_ID, Shift_Date, Start_Time, End_Time |
| maintenance_query | Query_ID, Clerk_ID, Mechanic_ID, Query_Desc, Date_Logged, Open, Progress, Closed |

## Files

- `rgi_trucking.sql` — Full database export (schema + data)
- `*.frm` / `*.ibd` — Raw MySQL InnoDB table files (MariaDB 10.4)

## How to Use

### Option 1: Import SQL (recommended)
```sql
mysql -u root < rgi_trucking.sql
```

### Option 2: Copy data files directly
Copy the `.frm` and `.ibd` files into your MySQL data directory (`/var/lib/mysql/rgi_trucking/` or `C:\xampp\mysql\data\rgi_trucking\`).

## Sample Data

- **Employees**: Phaahla (Admin)
- **Trucks**: Volvo FH16, Scania R500, MAN TGX, Mercedes Actros
- **Routes**: Pretoria–Johannesburg, Durban–Cape Town, Polokwane–Pretoria, Nelspruit–Maputo
- **Licences**: Code B, Code C, Code EC
