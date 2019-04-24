---
title: DeScription (propiedad, ADO)
TOCTitle: Description property (ADO)
ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15)
ms:contentKeyID: 48544064
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba6d05aa1bfb626520af60a30279983bae6fa566
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293934"
---
# <a name="description-property-ado"></a>DeScription (propiedad, ADO)


**Se aplica a:** Access 2013, Office 2013

Describe un objeto [Error](error-object-ado.md).

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de tipo **String** que contiene una descripción del error.

## <a name="remarks"></a>Comentarios

Use la propiedad **Description** para obtener una breve descripción del error. Muestre esta propiedad para alertar al usuario sobre un error que no puede o no desea controlar. La cadena procederá de ADO o de un proveedor.

Los proveedores son responsables de especificar el texto del error específico a ADO. ADO agrega un objeto [Error](error-object-ado.md) a la colección **Errors** por cada error o advertencia que recibe del proveedor. Enumere la colección **Errors** para rastrear los errores que especifica el proveedor.

