---
title: DrilledDown (propiedad, ADO MD)
TOCTitle: DrilledDown Property (ADO MD)
ms:assetid: 1dfe728f-8da2-1d2b-7361-8689a0b088b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248972(v=office.15)
ms:contentKeyID: 48543610
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f7e53eb2a6d1735e07fa73e38adad8a59522fddf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871503"
---
# <a name="drilleddown-property-ado-md"></a>DrilledDown (propiedad, ADO MD)


**Se aplica a**: Access 2013, Office 2013

Indica si no hay ningún elemento secundario que siga inmediatamente al elemento en el eje.

## <a name="return-values"></a>Valores devueltos

Devuelve un valor **Boolean** y es de solo lectura. **DrilledDown** devuelve **True** si no hay ningún elemento secundario del elemento activo en el eje. **DrilledDown** devuelve **False** si hay al menos un elemento secundario del elemento activo en el eje.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **DrilledDown** para determinar si hay al menos un elemento secundario de este elemento en el eje que siga inmediatamente a este elemento. Esta información es útil cuando se muestra el elemento.

Esta propiedad sólo es compatible con objetos [Member](member-object-ado-md.md) pertenecientes a un objeto [Position](position-object-ado-md.md). Si se hace referencia a esta propiedad desde objetos **Member** pertenecientes a un objeto [Level](level-object-ado-md.md), se produce un error.

