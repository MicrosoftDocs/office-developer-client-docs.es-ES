---
title: Workspace.Close Method (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 87f72a58cd3e24838416ef4d19ec1a2cf91e7c1f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483918"
---
# <a name="workspaceclose-method-dao"></a>Workspace.Close Method (DAO)


**Se aplica a**: Access 2013 | Office 2013

Cierra un objeto **Workspace** abierto.

## <a name="syntax"></a>Sintaxis

*expresión* . Cerrar

*expresión* Variable que representa un objeto **Workspace** .

## <a name="remarks"></a>Observaciones

Si el objeto **Workspace** ya está cerrado cuando utiliza **Close**, se produce un error en tiempo de ejecución.

Una alternativa al método **Close** es establecer el valor de una variable de objeto en **Nothing** (Set dbsTemp = Nothing).

