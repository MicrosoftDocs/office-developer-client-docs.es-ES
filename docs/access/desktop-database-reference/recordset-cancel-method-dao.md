---
title: Método Recordset.Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 102511575770ceb38cf682d5e627fb7e64faa1ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300815"
---
# <a name="recordsetcancel-method-dao"></a>Método Recordset.Cancel (DAO)


**Se aplica a:** Access 2013, Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . Cancelar

*expression* Variable que representa un objeto **Recordset**.

## <a name="remarks"></a>Comentarios

Use el **método Cancel** para finalizar la ejecución de una llamada asincrónica al método **Execute** o **OpenConnection** (es decir, el método se invocó con la opción dbRunAsync). **Cancel** devolverá un error en tiempo de ejecución si dbRunAsync no se usó en el método que estás intentando finalizar.

