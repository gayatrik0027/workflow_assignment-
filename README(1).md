# BPMN Camunda Assignment

This repository contains BPMN models created using **Camunda Modeler** for three business process scenarios.

## Tool Used

- **Camunda Modeler**
- **BPMN 2.0**

## Scenario 1: Employee Leave Approval

### Process Description

An employee submits a leave request through the company's HR system. The system checks the employee's available leave balance.

### BPMN Process Flow

1. Employee submits a leave request.
2. The HR system checks the leave balance.
3. An exclusive gateway checks whether sufficient leave balance is available.
4. If sufficient balance is available, the request is sent to the manager for approval.
5. If the manager approves the request:
   - The employee's leave balance is updated.
   - An approval notification is sent.
   - The process ends.
6. If the manager rejects the request:
   - A rejection notification is sent.
   - The process ends.
7. If there is insufficient leave balance:
   - An insufficient-balance notification is sent.
   - The process ends.

### BPMN Elements Used

- Start Event
- Tasks
- Exclusive Gateways
- Sequence Flows
- End Events

## Scenario 2: Online Purchase Order Processing

### Process Description

A customer places an online order. The system checks product availability and then processes the payment before preparing and shipping the order.

### BPMN Process Flow

1. Customer places an order.
2. The system checks product availability.
3. An exclusive gateway checks whether the product is available.
4. If the product is unavailable:
   - The customer is notified that the product is out of stock.
   - The process ends.
5. If the product is available:
   - The system processes the payment.
6. An exclusive gateway checks whether the payment is successful.
7. If payment fails:
   - The customer is notified about the payment failure.
   - The process ends.
8. If payment succeeds:
   - The order is confirmed and the product is prepared.
   - The order is shipped.
   - The customer receives a shipping confirmation.
   - The process ends.

### BPMN Elements Used

- Start Event
- Tasks
- Exclusive Gateways
- Sequence Flows
- Multiple Process Paths
- End Events

## Scenario 3: IT Service Request

### Process Description

An employee submits an IT support request. The help desk evaluates the severity of the problem and assigns it to the appropriate technician.

### BPMN Process Flow

1. Employee submits an IT support request.
2. The IT help desk receives the request.
3. The help desk checks the severity of the problem.
4. An exclusive gateway determines the severity.
5. For low or medium severity, the request is assigned to a support technician.
6. For high severity, the request is assigned to a senior technician.
7. The technician investigates the problem.
8. An exclusive gateway checks whether the problem has been resolved.
9. If the problem is resolved:
   - The technician fixes the problem.
10. If the problem cannot be resolved internally:
   - The problem is escalated to an external service provider.
11. The help desk updates the request status.
12. The employee receives a resolution notification.
13. The process ends.

### BPMN Elements Used

- Start Event
- Tasks
- Exclusive Gateways
- Sequence Flows
- Alternative Paths
- End Event

## Repository Contents

| File | Description |
|---|---|
| `BPMN_FINAL_Scenario1.bpmn` | Employee Leave Approval |
| `BPMN_FINAL_Scenario2.bpmn` | Online Purchase Order Processing |
| `BPMN_FINAL_Scenario3.bpmn` | IT Service Request |
| `README.md` | Assignment description and process explanations |

## Conclusion

The three BPMN models demonstrate how basic BPMN building blocks can be used to represent business processes, decisions, alternative process paths, notifications, and process completion.
