---
title: PageCount (propiedad, ADO)
TOCTitle: PageCount property (ADO)
ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15)
ms:contentKeyID: 48546609
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef5179f44a2c7c153411ae33566f3806f1e93573
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867373"
---
# <a name="pagecount-property-ado"></a>PageCount (propiedad, ADO)


**Se aplica a**: Access 2013, Office 2013

Indica cuántas páginas de datos contiene el objeto [Recordset](recordset-object-ado.md).

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de tipo **Long** que indica el número de páginas del objeto **Recordset**.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **NúmeroDePáginas (PageCount)** para determinar cuántas páginas de datos hay en el objeto **Recordset**. *Las páginas* son grupos de registros cuyo tamaño es igual que el valor de la propiedad [PageSize](pagesize-property-ado.md) . Aunque la última página esté incompleta debido a que existan menos registros que el valor **PageSize**, cuenta como una página adicional en el valor **NúmeroDePáginas (PageCount)**. Si el objeto **Recordset** no admite esta propiedad, el valor será -1 para indicar que **NúmeroDePáginas (PageCount)** es indeterminable.

Vea las propiedades **PageSize** y [AbsolutePage](absolutepage-property-ado.md) para obtener más información acerca de la funcionalidad de las páginas.

