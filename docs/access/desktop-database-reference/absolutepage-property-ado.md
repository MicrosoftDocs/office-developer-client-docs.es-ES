---
title: AbsolutePage (propiedad, ADO)
TOCTitle: AbsolutePage property (ADO)
ms:assetid: b6e5daac-cc21-0aa6-9119-a973595762bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15)
ms:contentKeyID: 48547288
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: a285f9f9533e4ecd903e6cc6c0e427bf44c84ca4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870537"
---
# <a name="absolutepage-property-ado"></a>AbsolutePage (propiedad, ADO)

**Se aplica a**: Access 2013, Office 2013

Indica en qué página reside el registro actual.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de **tipo Long** entre 1 y el número de páginas en el objeto [Recordset](recordset-object-ado.md) ([PageCount](pagecount-property-ado.md)) o bien, devuelve uno de los valores de [PositionEnum](positionenum.md) .

## <a name="remarks"></a>Comentarios

Esta propiedad puede usarse para identificar el número de página donde está ubicado el registro actual. Usa la propiedad [PageSize](pagesize-property-ado.md) para dividir lógicamente el número total de conjuntos de filas del objeto **Recordset** en series de páginas, cada una con un número de registros equivalente a **PageSize** (salvo en el caso de la última página, que puede tener menos registros). El proveedor debe admitir la funcionalidad apropiada para que esta propiedad esté disponible.

Al obtener o establecer la propiedad **AbsolutePage**, ADO usa la propiedad [AbsolutePosition](absoluteposition-property-ado.md) y la propiedad [PageSize](pagesize-property-ado.md) conjuntamente de la siguiente manera:

- Para obtener el valor de **AbsolutePage**, ADO recupera primero el valor de **AbsolutePosition** y, a continuación, lo divide entre el valor de **PageSize**.

- Para establecer el valor de **AbsolutePage**, ADO mueve **AbsolutePosition** de la siguiente forma: multiplica el valor de **PageSize** por el nuevo valor de **AbsolutePage** y, a continuación, le suma 1. Como resultado, la posición actual en el **objeto Recordset** después de establecer correctamente el valor de **AbsolutePage** es el primer registro de esa página.

Al igual que la propiedad **AbsolutePosition**, **AbsolutePage** se basa en 1 y es igual a 1 cuando el registro actual es el primer registro del objeto **Recordset**. Establezca esta propiedad para desplazarse al primer registro de una página determinada. Obtenga el número total de páginas de la propiedad **PageCount**.

