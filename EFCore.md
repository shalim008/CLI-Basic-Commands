dotnet --info
dotnet tool install --global dotnet-ef --version 3.1.3
dotnet ef -h
install Microsoft.EntityFrameworkCore.Design using NPM

cd API
dotnet ef migrations add InitialCreate -o Data/Migrations
dotnet ef database -h
dotnet ef database update
install SQLite

Microsoft.EntityFrameworkCore.SqlServer




############ Special Command ######
Drop Database : dotnet ef database drop -p Infrastructure -s API -c StoreContext
Remove Existing Migration: dotnet ef migrations remove -p Infrastructure -s API -c StoreContext

Add Migration DB: dotnet ef migrations add InithialCreate -p Infrastructure -s API -o Data/Migrations  -c StoreContext

Update Database: dotnet ef database update -p Infrastructure -s API -c StoreContext


######### Multiple DBContext migration command #############
Add New Migration Command
	- dotnet ef migrations add IdenttyInitial -p Infrastructure -s API -o Identity/Migrations -c AppIdentityDBContext

Remove Migration Command
	-dotenet ef migrations remove -p Infrastructure -s API  -c AppIdentityDBContext
