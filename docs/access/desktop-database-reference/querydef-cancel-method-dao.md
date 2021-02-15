---
title: Método QueryDef.Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: 91e61012-c01c-4c24-185c-bdadb7f33a58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197642(v=office.15)
ms:contentKeyID: 48546364
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1055470
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 56a4ba804dba25eb0b4722bcf5396229ee003f43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301123"
---
# <a name="querydefcancel-method-dao"></a>Método QueryDef.Cancel (DAO)


**Se aplica a:** Access 2013, Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . Cancelar

*expression* Variable que representa un objeto **QueryDef**.

## <a name="remarks"></a>Comentarios

Use el **método Cancel** para finalizar la ejecución de una llamada asincrónica al método **Execute** o **OpenConnection** (es decir, el método se invocó con la opción dbRunAsync). **Cancel** devolverá un error en tiempo de ejecución si dbRunAsync no se usó en el método que está intentando finalizar.

