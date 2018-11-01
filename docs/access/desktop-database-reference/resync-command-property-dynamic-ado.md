---
title: dinámica Resync Command (propiedad, ADO)
TOCTitle: Resync Command Property--Dynamic (ADO)
ms:assetid: 5c0c0819-620a-6eb0-a217-69113ec8d094
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249322(v=office.15)
ms:contentKeyID: 48545081
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 30707140284c4c4fda157e276e62666f0344ad14
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872007"
---
# <a name="resync-command-property--dynamic-ado"></a><span data-ttu-id="13391-102">dinámica Resync Command (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="13391-102">Resync Command Property--Dynamic (ADO)</span></span>

<span data-ttu-id="13391-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="13391-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="13391-104">Especifica una cadena de comando proporcionada por el usuario que el método [Resync](resync-method-ado.md) emite para actualizar los datos de la tabla especificada en la propiedad dinámica [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md).</span><span class="sxs-lookup"><span data-stu-id="13391-104">Specifies a user-supplied command string that the [Resync](resync-method-ado.md) method issues to refresh the data in the table named in the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) dynamic property.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="13391-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="13391-105">Settings and return values</span></span>

<span data-ttu-id="13391-106">Establece o devuelve un valor de tipo **String** que es una cadena de comandos.</span><span class="sxs-lookup"><span data-stu-id="13391-106">Sets or returns a **String** value which is a command string.</span></span>

## <a name="remarks"></a><span data-ttu-id="13391-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="13391-107">Remarks</span></span>

<span data-ttu-id="13391-108">El objeto [Recordset](recordset-object-ado.md) es el resultado de una operación JOIN ejecutada en varias tablas base.</span><span class="sxs-lookup"><span data-stu-id="13391-108">The [Recordset](recordset-object-ado.md) object is the result of a JOIN operation executed on multiple base tables.</span></span> <span data-ttu-id="13391-109">Las filas afectadas dependen del parámetro *AffectRecords* del método [Resync](resync-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="13391-109">The rows affected depend on the *AffectRecords* parameter of the [Resync](resync-method-ado.md) method.</span></span> <span data-ttu-id="13391-110">El método **Resync** estándar se ejecuta si las propiedades [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) y **Resync Command** no están establecidas.</span><span class="sxs-lookup"><span data-stu-id="13391-110">The standard **Resync** method is executed if the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) and **Resync Command** properties are not set.</span></span>

<span data-ttu-id="13391-p102">La cadena de comandos de la propiedad **Resync Command** es un comando con parámetros o un procedimiento almacenado que identifica de forma exclusiva a la fila que se va a actualizar y que devuelve una única fila que contiene el mismo número de columnas y en el mismo orden que la fila que se va a actualizar. La cadena de comandos contiene un parámetro por cada columna de clave principal de **Unique Table**; de lo contrario, se devuelve un error en tiempo de ejecución. Los parámetros no se rellenan automáticamente con los valores de clave principal de la fila que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="13391-p102">The command string of the **Resync Command** property is a parameterized command or stored procedure that uniquely identifies the row being refreshed, and returns a single row containing the same number and order of columns as the row to be refreshed. The command string contains a parameter for each primary key column in the **Unique Table**; otherwise, a run-time error is returned. The parameters are automatically filled in with primary key values from the row to be refreshed.</span></span>

<span data-ttu-id="13391-114">A continuación se muestran dos ejemplos basados en SQL:</span><span class="sxs-lookup"><span data-stu-id="13391-114">Here are two examples based on SQL:</span></span>

1.  <span data-ttu-id="13391-115">**Recordset** se define mediante un comando:</span><span class="sxs-lookup"><span data-stu-id="13391-115">The **Recordset** is defined by a command:</span></span>

    ```sql
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE city = Seattle
        ORDER BY CustomerID
    ```

    <span data-ttu-id="13391-116">Se establece la propiedad **Resync Command** en:</span><span class="sxs-lookup"><span data-stu-id="13391-116">The **Resync Command** property is set to:</span></span>

    ```sql
     SELECT * FROM 
        (SELECT * FROM Customers JOIN Orders 
        ON Customers.CustomerID = Orders.CustomerID
        city = Seattle ORDER BY CustomerID)
     WHERE Orders.OrderID = ?"
    ```

    <span data-ttu-id="13391-p103">**Unique Table** es *Orders* y la clave principal, *OrderID*, tiene parámetros. La subselección proporciona una forma simple de garantizar mediante programación que se devuelve el mismo número de columnas y en el mismo orden que con el comando original.</span><span class="sxs-lookup"><span data-stu-id="13391-p103">The **Unique Table** is *Orders* and its primary key, *OrderID*, is parameterized. The sub-select provides a simple way to programmatically ensure that the same number and order of columns are returned as by the original command.</span></span>

2. <span data-ttu-id="13391-119">**Recordset** es definido por un procedimiento almacenado:</span><span class="sxs-lookup"><span data-stu-id="13391-119">The **Recordset** is defined by a stored procedure:</span></span>

    ```sql
        CREATE PROC Custorders @CustomerID char(5) AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID 
        WHERE Customers.CustomerID = @CustomerID
    ```

    <span data-ttu-id="13391-120">El método **Resync** debe ejecutar el siguiente procedimiento almacenado:</span><span class="sxs-lookup"><span data-stu-id="13391-120">The **Resync** method should execute the following stored procedure:</span></span>

    ```sql
        CREATE PROC CustordersResync @ordid int AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE Orders.ordid  = @ordid
    ```

    <span data-ttu-id="13391-121">Se establece la propiedad **Resync Command** en:</span><span class="sxs-lookup"><span data-stu-id="13391-121">The **Resync Command** property is set to:</span></span>

    `"{call CustordersResync (?)}"`

<span data-ttu-id="13391-122">Una vez más, **Unique Table** es *Orders* y la clave principal, *OrderID*, tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="13391-122">Once again, the **Unique Table** is *Orders* and its primary key, *OrderID*, is parameterized.</span></span>

<span data-ttu-id="13391-123">**Resync Command** es una propiedad dinámica que se anexa a la colección **Properties** del objeto [Recordset](properties-collection-ado.md) cuando la propiedad [CursorLocation](cursorlocation-property-ado.md) está establecida en **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="13391-123">**Resync Command** is a dynamic property appended to the **Recordset** object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

