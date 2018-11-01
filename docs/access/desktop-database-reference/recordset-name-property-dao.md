---
title: Recordset.Name Property (DAO)
TOCTitle: Name Property
ms:assetid: 2a80b994-a135-cd61-3906-17dfa0580110
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192067(v=office.15)
ms:contentKeyID: 48543910
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e58b422165a1530a8ceb65298f0cac81d558c2a6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870229"
---
# <a name="recordsetname-property-dao"></a>Recordset.Name Property (DAO)


**Se aplica a**: Access 2013, Office 2013

Devuelve el nombre del objeto especificado. **String** de sólo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . Nombre

*expresión* Variable que representa un objeto **Recordset** .

## <a name="remarks"></a>Observaciones

La propiedad **Name** de un objeto **Recordset** abierto mediante una instrucción SQL es los primeros 256 caracteres de la instrucción SQL.

