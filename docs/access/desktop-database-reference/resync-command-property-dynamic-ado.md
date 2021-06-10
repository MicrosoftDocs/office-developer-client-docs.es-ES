---
title: Propiedad dinámica Resync Command (ADO)
TOCTitle: Resync Command dynamic property (ADO)
ms:assetid: 5c0c0819-620a-6eb0-a217-69113ec8d094
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249322(v=office.15)
ms:contentKeyID: 48545081
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa1fe05e6aa7edf04ad74864eb30a03403323c8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306583"
---
# <a name="resync-command-dynamic-property-ado"></a><span data-ttu-id="b4b85-102">Propiedad dinámica Resync Command (ADO)</span><span class="sxs-lookup"><span data-stu-id="b4b85-102">Resync Command dynamic property (ADO)</span></span>

<span data-ttu-id="b4b85-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4b85-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b4b85-104">Especifica una cadena de comando proporcionada por el usuario que el método [Resync](resync-method-ado.md) emite para actualizar los datos de la tabla especificada en la propiedad dinámica [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b4b85-104">Specifies a user-supplied command string that the [Resync](resync-method-ado.md) method issues to refresh the data in the table named in the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) dynamic property.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="b4b85-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="b4b85-105">Settings and return values</span></span>

<span data-ttu-id="b4b85-106">Establece o devuelve un valor de tipo **String** que es una cadena de comandos.</span><span class="sxs-lookup"><span data-stu-id="b4b85-106">Sets or returns a **String** value which is a command string.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4b85-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b4b85-107">Remarks</span></span>

<span data-ttu-id="b4b85-p101">El objeto [Recordset](recordset-object-ado.md) es el resultado de una operación JOIN ejecutada en varias tablas base. Las filas afectadas dependen del parámetro *AffectRecords* del método [Resync](resync-method-ado.md). El método **Resync** estándar se ejecuta si las propiedades [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) y **Resync Command** no están establecidas.</span><span class="sxs-lookup"><span data-stu-id="b4b85-p101">The [Recordset](recordset-object-ado.md) object is the result of a JOIN operation executed on multiple base tables. The rows affected depend on the *AffectRecords* parameter of the [Resync](resync-method-ado.md) method. The standard **Resync** method is executed if the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) and **Resync Command** properties are not set.</span></span>

<span data-ttu-id="b4b85-p102">La cadena de comandos de la propiedad **Resync Command** es un comando con parámetros o un procedimiento almacenado que identifica de forma exclusiva a la fila que se va a actualizar y que devuelve una única fila que contiene el mismo número de columnas y en el mismo orden que la fila que se va a actualizar. La cadena de comandos contiene un parámetro por cada columna de clave principal de **Unique Table**; de lo contrario, se devuelve un error en tiempo de ejecución. Los parámetros no se rellenan automáticamente con los valores de clave principal de la fila que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="b4b85-p102">The command string of the **Resync Command** property is a parameterized command or stored procedure that uniquely identifies the row being refreshed, and returns a single row containing the same number and order of columns as the row to be refreshed. The command string contains a parameter for each primary key column in the **Unique Table**; otherwise, a run-time error is returned. The parameters are automatically filled in with primary key values from the row to be refreshed.</span></span>

<span data-ttu-id="b4b85-114">A continuación se muestran dos ejemplos basados en SQL:</span><span class="sxs-lookup"><span data-stu-id="b4b85-114">Here are two examples based on SQL:</span></span>

1.  <span data-ttu-id="b4b85-115">**Recordset** se define mediante un comando:</span><span class="sxs-lookup"><span data-stu-id="b4b85-115">The **Recordset** is defined by a command:</span></span>

    ```sql
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE city = Seattle
        ORDER BY CustomerID
    ```

    <span data-ttu-id="b4b85-116">Se establece la propiedad **Resync Command** en:</span><span class="sxs-lookup"><span data-stu-id="b4b85-116">The **Resync Command** property is set to:</span></span>

    ```sql
     SELECT * FROM 
        (SELECT * FROM Customers JOIN Orders 
        ON Customers.CustomerID = Orders.CustomerID
        city = Seattle ORDER BY CustomerID)
     WHERE Orders.OrderID = ?"
    ```

    <span data-ttu-id="b4b85-p103">**Unique Table** es *Orders* y la clave principal, *OrderID*, tiene parámetros. La subselección proporciona una forma simple de garantizar mediante programación que se devuelve el mismo número de columnas y en el mismo orden que con el comando original.</span><span class="sxs-lookup"><span data-stu-id="b4b85-p103">The **Unique Table** is *Orders* and its primary key, *OrderID*, is parameterized. The sub-select provides a simple way to programmatically ensure that the same number and order of columns are returned as by the original command.</span></span>

2. <span data-ttu-id="b4b85-119">**Recordset** es definido por un procedimiento almacenado:</span><span class="sxs-lookup"><span data-stu-id="b4b85-119">The **Recordset** is defined by a stored procedure:</span></span>

    ```sql
        CREATE PROC Custorders @CustomerID char(5) AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID 
        WHERE Customers.CustomerID = @CustomerID
    ```

    <span data-ttu-id="b4b85-120">El método **Resync** debe ejecutar el siguiente procedimiento almacenado:</span><span class="sxs-lookup"><span data-stu-id="b4b85-120">The **Resync** method should execute the following stored procedure:</span></span>

    ```sql
        CREATE PROC CustordersResync @ordid int AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE Orders.ordid  = @ordid
    ```

    <span data-ttu-id="b4b85-121">Se establece la propiedad **Resync Command** en:</span><span class="sxs-lookup"><span data-stu-id="b4b85-121">The **Resync Command** property is set to:</span></span>

    `"{call CustordersResync (?)}"`

<span data-ttu-id="b4b85-122">Una vez más, **Unique Table** es *Orders* y la clave principal, *OrderID*, tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b4b85-122">Once again, the **Unique Table** is *Orders* and its primary key, *OrderID*, is parameterized.</span></span>

<span data-ttu-id="b4b85-123">**Resync Command** es una propiedad dinámica que se anexa a la colección [Properties](properties-collection-ado.md) del objeto **Recordset** cuando la propiedad [CursorLocation](cursorlocation-property-ado.md) está establecida en **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="b4b85-123">**Resync Command** is a dynamic property appended to the **Recordset** object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

