---
title: DBEngine.DefaultType Property (DAO)
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
ms.openlocfilehash: d32c0860f76aeeaa64a060a55579d05c1eb571ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485304"
---
# <a name="dbenginedefaulttype-property-dao"></a>DBEngine.DefaultType Property (DAO)


**Se aplica a**: Access 2013 | Office 2013

Establece o devuelve un valor que indica qué tipo de área de trabajo se utilizará en el siguiente objeto **[Workspace](workspace-object-dao.md)** que se cree.

## <a name="syntax"></a>Sintaxis

*expresión* . DefaultType

*expresión* Variable que representa un objeto **DBEngine** .

## <a name="remarks"></a>Observaciones

La configuración o el valor devuelto puede ser una de las constantes **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)**.


> [!NOTE]
> <P>[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</P>



El valor se puede invalidar para un único **Workspace** estableciendo el argumento type en el método **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** .

