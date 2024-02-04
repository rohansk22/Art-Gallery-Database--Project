# Art-Gallery-Database 

| SL.NO. |	TABLE NAME	| TABLE DESCRIPTION |
| ------ |:------------:|:-----------------:|
|   1    | ArtistInfoT	| Record of Artist’s personal information |
|   2	   | ArtistContractT |	Details of an artist’s contract with the art gallery |
|   3    | EmployeeInfoT |	Record of the gallery’s employees |
|   4	   | PartnerOrgT	| Record of partner organisations – janitorial, catering and easte disposal |
|   5	   | CustomerInfoT |	Details of Customer’s personal information |
|   6    |	ProductInfoT |	Record of gallery’s souveniers, art pieces and newsletters |
|   7	   | InventoryArtT |	Details of an artwork- artists and the date of installments |
|   8	   | CustomerInterestT |	A Customer’s enquiry about product so as to implement recommender systems |
|   9	   | DisplayArtT |	Record of an item’s location |
|  10	   | LedgerT	| Record of every transaction made every day |
|  11	   | CreditT	| Record of cash inflow <br> 	Automatically updates credit entry from ledger </br> |
|  12	   | DebitT	| Record of cash outflow <br> 	Automatically updates debit entry from ledger </br> |
|  13    |	CollabT |	Record of events hosted by the art gallery in collaboration with other institutes |
|  14	   |  SalesT	| Record of sales made by salesman to a customer |
|  15	   | Artistcontract_auditT	| Automatically updates an artists contract renewal |
|  16	   | partnerOrg_auditT |	Automatically updates a partner organisation’s last date with the gallery |
|  17	   | EventT	| Record of events hosted by the art gallery |


There are: <br>
**2 Functions:** <br>
> TotalPurchase(): To return the total purchase amount of a customer. <br>
> TotalSales(): To return the total sales made by an artist <br>


**3 Stored Procedures:** <br>
> GetCustomerLevel(): Classifies customers based on their purchase amount - Silver, Gold and Platinum <br>
> GetArtistLevel(): Classifies artists based on their purchase amount - Rookie, Novice, Expert, Genius <br>
> GetPlanner(): Shows all the events taking place on a particular date <br>

**4 Triggers:** <br>
> artistContract_UpdateT: It is a pre update trigger that stores all the details of an artist who renews his contract with the gallery <br>
> pastPartnerOrg deleteT: This is a pre delete trigger which stores the information of a partner when he leaves the organization <br>
> ledger_CreditT: A post insert trigger that checks the value of a new record and stores the information into the credit if transaction amount> 0, or debit, if transaction amount<0 <br>
> salesT: A pre insert trigger that updates the sales table based on a transaction <br>

