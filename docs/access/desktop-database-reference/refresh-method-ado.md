---
title: Refresh (método, ADO)
TOCTitle: Refresh Method (ADO)
ms:assetid: f1c8829f-9c7d-12b6-7470-727ff38d663e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250227(v=office.15)
ms:contentKeyID: 48548631
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1ea277f83c39bde4b5309a26b87961ff2325b145
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483568"
---
# <a name="refresh-method-ado"></a>Refresh (método, ADO)


**Se aplica a**: Access 2013 | Office 2013

Actualiza los objetos de una colección para reflejar los objetos disponibles y específicos del proveedor.

## <a name="syntax"></a>Sintaxis

*colección*. Actualización

## <a name="remarks"></a>Comentarios

El método **Refresh** realiza diferentes tareas según la colección desde la que se llame al método.

## <a name="parameters"></a>Parámetros

Si se usa el método **Refresh** en la colección [Parameters](command-object-ado.md) de un objeto [Command](parameters-collection-ado.md), se recupera la información de parámetros del proveedor para el procedimiento almacenado o la consulta parametrizada especificada en el objeto **Command**. La colección estará vacía para los proveedores que no admitan llamadas a procedimientos almacenados o consultas parametrizadas.

La propiedad [ActiveConnection](activeconnection-property-ado.md) del objeto **Command** debe establecerse en un objeto [Connection](connection-object-ado.md) válido, la propiedad [CommandText](commandtext-property-ado.md) en un comando válido y la propiedad [CommandType](commandtype-property-ado.md) en **adCmdStoredProc** antes de llamar al método **Refresh**.

Si obtiene acceso a la colección **Parameters** antes de llamar al método **Refresh**, ADO llamará automáticamente al método y rellenará la colección.


> [!NOTE]
> <P>[!NOTA] Si utiliza el método <STRONG>Refresh</STRONG> para obtener información de parámetros del proveedor y se devuelve uno o varios objetos <A href="parameter-object-ado.md">Parameter</A> de longitud variable, puede que ADO asigne memoria para los parámetros en función de su posible tamaño máximo, lo que provocará un error durante la ejecución. Debe establecer explícitamente la propiedad <A href="size-property-ado.md">Size</A> de estos parámetros antes de llamar al método <A href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execute</A> para evitar errores.</P>



**Fields**

Utilizar el método **Refresh** en la colección **Fields** no tiene ningún efecto visible. Para recuperar los cambios de la estructura de base de datos subyacente, debe utilizar el método [Requery](requery-method-ado.md) o, si el objeto [Recordset](recordset-object-ado.md) no admite marcadores, el método [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md).

**Properties**

Si utiliza el método **Refresh** en una colección **Properties** de algunos objetos, se rellena la colección con las propiedades dinámicas que expone el proveedor. Estas propiedades proporcionan información acerca de la funcionalidad específica del proveedor, aparte de las propiedades integradas que ADO admite.

