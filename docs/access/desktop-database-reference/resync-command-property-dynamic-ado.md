---
title: dinámica Resync Command (propiedad, ADO)
TOCTitle: Resync Command Property--Dynamic (ADO)
ms:assetid: 5c0c0819-620a-6eb0-a217-69113ec8d094
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249322(v=office.15)
ms:contentKeyID: 48545081
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d9133f37b236cfa876a5d6ae8642f25f919f2cb
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602807"
---
# <a name="resync-command-property--dynamic-ado"></a>dinámica Resync Command (propiedad, ADO)

**Se aplica a**: Access 2013 | Office 2013

Especifica una cadena de comando proporcionada por el usuario que el método [Resync](resync-method-ado.md) emite para actualizar los datos de la tabla especificada en la propiedad dinámica [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md).

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
=======
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
>>>>>>> master

Establece o devuelve un valor de tipo **String** que es una cadena de comandos.

## <a name="remarks"></a>Comentarios

El objeto [Recordset](recordset-object-ado.md) es el resultado de una operación JOIN ejecutada en varias tablas base. Las filas afectadas dependen del parámetro *AffectRecords* del método [Resync](resync-method-ado.md) . El método **Resync** estándar se ejecuta si las propiedades [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) y **Resync Command** no están establecidas.

La cadena de comandos de la propiedad **Resync Command** es un comando con parámetros o un procedimiento almacenado que identifica de forma exclusiva a la fila que se va a actualizar y que devuelve una única fila que contiene el mismo número de columnas y en el mismo orden que la fila que se va a actualizar. La cadena de comandos contiene un parámetro por cada columna de clave principal de **Unique Table**; de lo contrario, se devuelve un error en tiempo de ejecución. Los parámetros no se rellenan automáticamente con los valores de clave principal de la fila que se va a actualizar.

A continuación se muestran dos ejemplos basados en SQL:

1.  **Recordset** se define mediante un comando:

    ```sql
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE city = Seattle
        ORDER BY CustomerID
    ```

    Se establece la propiedad **Resync Command** en:

    ```sql
     SELECT * FROM 
        (SELECT * FROM Customers JOIN Orders 
        ON Customers.CustomerID = Orders.CustomerID
        city = Seattle ORDER BY CustomerID)
     WHERE Orders.OrderID = ?"
    ```

    **Unique Table** es *Orders* y la clave principal, *OrderID*, tiene parámetros. La subselección proporciona una forma simple de garantizar mediante programación que se devuelve el mismo número de columnas y en el mismo orden que con el comando original.

2. **Recordset** es definido por un procedimiento almacenado:

    ```sql
        CREATE PROC Custorders @CustomerID char(5) AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID 
        WHERE Customers.CustomerID = @CustomerID
    ```

    El método **Resync** debe ejecutar el siguiente procedimiento almacenado:

    ```sql
        CREATE PROC CustordersResync @ordid int AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE Orders.ordid  = @ordid
    ```

    Se establece la propiedad **Resync Command** en:

    `"{call CustordersResync (?)}"`

Una vez más, **Unique Table** es *Orders* y la clave principal, *OrderID*, tiene parámetros.

**Resync Command** es una propiedad dinámica que se anexa a la colección **Properties** del objeto [Recordset](properties-collection-ado.md) cuando la propiedad [CursorLocation](cursorlocation-property-ado.md) está establecida en **adUseClient**.

