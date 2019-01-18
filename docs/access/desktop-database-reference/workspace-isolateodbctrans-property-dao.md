---
title: Propiedad Workspace.IsolateODBCTrans (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 781679dfbd4050cfde219802db4cd9e1544d83ae
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701560"
---
# <a name="workspaceisolateodbctrans-property-dao"></a>Propiedad Workspace.IsolateODBCTrans (DAO)


**Se aplica a**: Access 2013, Office 2013

Establece o devuelve un valor que indica si varias transacciones que implican los mismos motores de base de datos de Microsoft Access conectados al origen de datos ODBC están aisladas (sólo para áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . IsolateODBCTrans

*expresión* Variable que representa un objeto **Workspace** .

## <a name="remarks"></a>Observaciones

En algunas situaciones, necesitará tener simultáneamente varias transacciones pendientes de la misma conexión ODBC. Para esto, debe abrir un **Workspace** distinto para cada transacción. Aunque cada **Workspace** puede tener su propia conexión ODBC a la base de datos, ello puede hacer descender el rendimiento del sistema. Como normalmente el aislamiento de la transacción no es necesario, las conexiones ODBC desde varios objetos **Workspace** abiertos por el mismo usuario se comparten de forma predeterminada.

Algunos servidores ODBC, como Microsoft SQL Server, no permiten transacciones simultáneas en una sola conexión. Si necesita tener más de una transacción pendiente a la vez en una base de datos, establezca la propiedad **IsolateODBCTrans** en **True** para cada **Workspace** tan pronto como abra la propiedad. Con ello se fuerza una conexión ODBC individual para cada **Workspace**.

