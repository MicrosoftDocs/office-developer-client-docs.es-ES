---
title: Recordset2.Cancel (método) (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 159f476b592a8c944df2dc4570d84377c89b5043
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929237"
---
# <a name="recordset2cancel-method-dao"></a>Recordset2.Cancel (método) (DAO)


**Se aplica a**: Access 2013, Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . Cancelar

*expresión* Expresión que devuelve un objeto **Recordset2** .

## <a name="remarks"></a>Comentarios

Utilice el método **Cancel** para finalizar la ejecución de una llamada al método **Execute** u **OpenConnection** asincrónica (es decir, el método se abrió con la opción dbRunAsync). **Cancel** devolverá un error en tiempo de ejecución si no se utilizó dbRunAsync en el método que está intentando terminar.

