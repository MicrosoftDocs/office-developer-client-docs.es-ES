---
title: Propiedad DrilledDown (ADO MD)
TOCTitle: DrilledDown property (ADO MD)
ms:assetid: 1dfe728f-8da2-1d2b-7361-8689a0b088b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248972(v=office.15)
ms:contentKeyID: 48543610
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 40a97c7f755f681169c77c3a2077ee41d9cdc980
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293689"
---
# <a name="drilleddown-property-ado-md"></a>Propiedad DrilledDown (ADO MD)


**Se aplica a:** Access 2013, Office 2013

Indica si no hay ningún elemento secundario que siga inmediatamente al elemento en el eje.

## <a name="return-values"></a>Valores devueltos

Devuelve un valor **Boolean** y es de solo lectura. **DrilledDown** devuelve **True** si no hay ningún elemento secundario del elemento activo en el eje. **DrilledDown** devuelve **False** si hay al menos un elemento secundario del elemento activo en el eje.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **DrilledDown** para determinar si hay al menos un elemento secundario de este elemento en el eje que siga inmediatamente a este elemento. Esta información es útil cuando se muestra el elemento.

Esta propiedad sólo es compatible con objetos [Member](member-object-ado-md.md) pertenecientes a un objeto [Position](position-object-ado-md.md). Si se hace referencia a esta propiedad desde objetos **Member** pertenecientes a un objeto [Level](level-object-ado-md.md), se produce un error.

