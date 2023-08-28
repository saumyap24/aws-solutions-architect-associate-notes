- [Reserved Instances (RI)](#reserved-instances-ri)
    - [Term](#term)
    - [Class](#class)
    - [Payment Options](#payment-options)
- [Reserved Instances Attributes](#reserved-instance-ri-attributes)
- [Regional and Zonal RI](#regional-and-zonal-ri)
- [RI Limits](#ri-limits)
- [Capacity Reservations](#capacity-reservations)
- [Standard vs Convertible RI](#standard-vs-convertible-ri)
- [RI Marketplace](#ri-marketplace)

---
## Reserved Instances (RI)

- Designed for applications that have a <b><ins> steady state,</ins> <ins> predictable usage</ins> </b> or require <b><ins> reserved capacity.</ins> </b>
- Reduced Pricing is based on <b> Term</b> x <b>Class Offering </b> x <b>Payment Option </b>
    - ### Term
        - <i>{The longer the term the greater the savings}</i>
        - Commit to <ins> 1 year  or 3 Year contract </ins>
        - Reserved Instances do not renew automatically
        - When it is <ins> expired it will use on-demand </ins> with no interruption to service
    - ### Class 
        - <i> {The less flexible the greater savings} </i>
        - <b> Standard </b>
            - Up to 75% reduced pricing compared to on-demand
            - Can modify RI attributes
        - <b> Convertible </b>
            - Up to 54% reduced pricing compared to on-demand
            - can exchange RI based on RI attributes if greater or equal in value
        - <strike> <b> Scheduled </b></strike>
            - AWS no longer offers Scheduled RI
    - ### Payment Options
        - <i> {The greater upfront the greater savings} </i>
        - <b> All upfront </b> : full payment at the start
        - <b> Partial Upfront </b> : A portion of the cost must be paid and remaining hours billed at a discounted hourly rate
        - <b> No Upfront </b> : billed at a discounted hourly rate for every hour within the term,regardless of whether the Reserved Instance is being used
    - <i><ins> RIs can be shared between multiple accounts within AWS organization </ins> </i>
    - <b>Unused RIs </b> can be sold in the <ins><i> Reserved Instance Marketplace</i></ins>

---
## Reserved Instance (RI) Attributes 
--- 
- RI attributes
    - are limited based on class offering and can affect the final price of an RI instance
    - 4 RI attributes:
        - <b>Instance Type:</b>
            - eg. m4.Large. This is composed of the instance family (for example , m4) and the instance size (for example large)
        - <b> Region:</b>
            - The region in which the Reserved Instance is purchased
        - <b>Tenancy:</b>
            - Whether your instance runs on shared(default) or single-tenant (dedicated) hardware
        - <b>Platform:</b>
            - the operating system eg. Windows or Linux/Unix

---
## Regional and Zonal RI
---
| Regional RI : purchase for a region                         | Zonal RI : purchase for an Availability Zone                                       |
| ----------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| does not reserve capacity | reserves capacity in the specified Availability Zone |
| RI discount applies to instance usage in <ins> any AZ</ins> in the Region | RI discount applies to instance in the <ins> selected AZ </ins> (No AZ Flexibility) |
| Ri discount applied to instance usage within the instance family, regardless of size. Only supported n Amazon Linux, Unix Reserved Instances with default tenancy | No instance size flexibility </br>  Ri discounts applies to instance usage for the specified instance type and size only </br>  |
| You can queue purchases for regional RI  | You can't queue purchases for Zonal RI | 

---
## RI Limits 
---
- There is a limit to the number of Reserved Instances that you can purchase per month
    - Per month you can purchase
        - 20 Regional Reserved Instances per Region
        - 20 Zonal Reserved Instances per AZ

| Regional Limits | Zonal Limits | 
| --------------- | ------------ |
| You cannot exceed your running On-Demand Instance limit by purchasing regional Reserved Instances. The default On-Demand Instance limit is 20.  | You can exceed your running On-Demand Instance limit by purchasing zonal Reserved Instances| 
| Before purchasing RI ensure On-Demand limit is equal to or greater than your RI you intend to purchase | If you already have 20 running On-Demand Instances, and you purchase 20 Zonal Reserved Instances, you can launch a further 20 On-Demand Instances that match the specifications of your zonal Reserved Instances |

---
## Capacity Reservations 
---
- EC2 instances are backed by different kind of hardware, and so there is a finite amount of servers available within an Availability Zone per instance type or family 
- You go to launch a specific type of EC2 instance but AWS has ran out of that server
- Capacity reservation is a service of EC2 that allows you to request a reserve of EC2 instance type for a specific Region and AZ

---
## Standard vs Convertible RI
---

| Standard  RI | Convertible RI |
| ------------ | -------------- |
| RI attributes can be modified </br> -  Change the AZ within same Region </br> - Change the scope of the Zonal RI to Regional RI or visa versa </br> - Change the instance size (Linux/Unix only, default tenancy) </br> - Change network from Ec2-Classic to VPC and visa versa | RI attributes can't be modified (you perform an exchange) |
| Can't be exchanged | Can be exchanged during the term for another Convertible RI with new RI attributes, including: </br> - Instance type </br> - Instance Family </br> - Platform </br> - Scope </br> - Tenancy |
| Can be bought or sold in the RI Marketplace | Can't be bought or Sold in the RI Marketplace |

---
## RI Marketplace
---
- EC2 Reserved Instance Marketplace allows you to sell your unused Standard RI to recoup your RI spend for RI you do not intend or cannot use 

- Reserved Instances can be sold after they have been active for at least 30 days and once AWS has received the upfront payment (if applicable)
- You must have a US bank account to sell Reserved Instances on the Reserved Instance Marketplace
- There must be at least one month remaining in the term of the Reserved Instance you are listing
- You will retain the pricing and capacity benefit of your reservation until it's sold and the transaction is complete 
- Your company name ( and address upon request) will be shared with the buyer for tax purposes.
- A seller can set only the upfront price for a Reserved Instance. The usage price and other configuration (eg. instance type, availability zone, platform) will remain the same as when the Reserved Instance was initially purchased 
-  The term length will be rounded down to the nearest month. For example, a reservation with 9 months and 15 days remaining will appear as 9 months on the Reserved Instance Marketplace.
- You can sell upto $20,000 in Reserved Instances per year. If you need to sell more Reserved Instances
- Reserved Instances in the GovCloud region cannot be sold on the Reserved Instance Marketplace

