---
title: 'Método Clear: ActiveX Data Objects (ADO)'
TOCTitle: Clear method (ADO)
ms:assetid: 5d51f42c-147b-1fcf-d05b-123e5714ecb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249329(v=office.15)
ms:contentKeyID: 48545110
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b0d76480bdb5d5a3ab258e103a00707af303a4d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296363"
---
# <a name="clear-method-ado"></a>Método Clear (ADO)


**Se aplica a:** Access 2013, Office 2013

Quita todos los objetos **Error** de la colección **Errors**.

## <a name="syntax"></a>Sintaxis

*Errores*. Borrar

## <a name="remarks"></a>Comentarios

Utilice el método **Clear** en la colección [Errors](errors-collection-ado.md) para quitar todos los objetos [Error](error-object-ado.md) de la colección. Cuando se produce un error, ADO borra automáticamente la colección **Errors** y la rellena con objetos **Error** basándose en el nuevo error.

Algunos métodos y propiedades devuelven advertencias que aparecen como objetos **Error** en la colección **Errors** pero que no detienen la ejecución de un programa. Antes de llamar a los métodos [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) o [CancelBatch](cancelbatch-method-ado.md) en un objeto [Recordset](recordset-object-ado.md), antes de llamar al método [Open](open-method-ado-connection.md) en un objeto [Connection](connection-object-ado.md), y antes de establecer la propiedad [Filter](filter-property-ado.md) de un objeto **Recordset**, llame al método **Clear** en la colección **Errors**. De este modo, podrá leer la propiedad [Count](count-property-ado.md) de la colección **Errors** y comprobar si hay advertencias devueltas.

