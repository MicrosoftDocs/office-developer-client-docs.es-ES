---
title: Recordset.Cancel Method (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1d7e77bd844385b9400449027312dacc02940e58
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484041"
---
# <a name="recordsetcancel-method-dao"></a>Recordset.Cancel Method (DAO)


**Se aplica a**: Access 2013 | Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . Cancelar

*expresión* Variable que representa un objeto **Recordset** .

## <a name="remarks"></a>Comentarios

Utilice el método **Cancel** para finalizar la ejecución de una llamada al método **Execute** u **OpenConnection** asincrónica (es decir, el método se abrió con la opción dbRunAsync). **Cancel** devolverá un error en tiempo de ejecución si no se utilizó dbRunAsync en el método que está intentando terminar.

