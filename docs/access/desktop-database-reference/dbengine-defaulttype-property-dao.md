---
title: Propiedad DBEngine.DefaultType (DAO)
TOCTitle: DefaultType Property
ms:assetid: b4371f3e-1ce0-1d0f-93a8-0c5329b510ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822060(v=office.15)
ms:contentKeyID: 48547217
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053580
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 23f6c87ede6da2cc5b2f3203bfa13cb17bf93e82
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713593"
---
# <a name="dbenginedefaulttype-property-dao"></a>Propiedad DBEngine.DefaultType (DAO)


**Se aplica a**: Access 2013, Office 2013

Establece o devuelve un valor que indica qué tipo de área de trabajo se utilizará en el siguiente objeto **[Workspace](workspace-object-dao.md)** que se cree.

## <a name="syntax"></a>Sintaxis

*expresión* . DefaultType

*expresión* Variable que representa un objeto **DBEngine** .

## <a name="remarks"></a>Observaciones

La configuración o el valor devuelto puede ser una de las constantes **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)**.


> [!NOTE]
> [!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.

El valor se puede invalidar para un único **Workspace** estableciendo el argumento type en el método **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** .

