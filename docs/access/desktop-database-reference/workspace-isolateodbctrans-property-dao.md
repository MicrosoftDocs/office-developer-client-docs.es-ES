---
title: Workspace.IsolateODBCTrans Property (DAO)
TOCTitle: IsolateODBCTrans Property
ms:assetid: f7a48358-870b-cad3-d4ef-e46b50428e12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836924(v=office.15)
ms:contentKeyID: 48548770
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053083
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8a2696dfabe609042c920b33b2a0f5fd696d9833
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483356"
---
# <a name="workspaceisolateodbctrans-property-dao"></a>Workspace.IsolateODBCTrans Property (DAO)


**Se aplica a**: Access 2013 | Office 2013

Establece o devuelve un valor que indica si varias transacciones que implican los mismos motores de base de datos de Microsoft Access conectados al origen de datos ODBC están aisladas (sólo para áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . IsolateODBCTrans

*expresión* Variable que representa un objeto **Workspace** .

## <a name="remarks"></a>Observaciones

En algunas situaciones, necesitará tener simultáneamente varias transacciones pendientes de la misma conexión ODBC. Para esto, debe abrir un **Workspace** distinto para cada transacción. Aunque cada **Workspace** puede tener su propia conexión ODBC a la base de datos, ello puede hacer descender el rendimiento del sistema. Como normalmente el aislamiento de la transacción no es necesario, las conexiones ODBC desde varios objetos **Workspace** abiertos por el mismo usuario se comparten de forma predeterminada.

Algunos servidores ODBC, como Microsoft SQL Server, no permiten transacciones simultáneas en una sola conexión. Si necesita tener más de una transacción pendiente a la vez en una base de datos, establezca la propiedad **IsolateODBCTrans** en **True** para cada **Workspace** tan pronto como abra la propiedad. Con ello se fuerza una conexión ODBC individual para cada **Workspace**.

