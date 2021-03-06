---
title: DetenerTodasMacros (acción de macro)
TOCTitle: StopAllMacros macro action
ms:assetid: 6afbf906-03b8-6e68-bbc9-7a4b141cf1c5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195440(v=office.15)
ms:contentKeyID: 48545442
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm104968
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4e44182dd4290b05a2cfc8fabdf9240819f4b7aa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314479"
---
# <a name="stopallmacros-macro-action"></a>DetenerTodasMacros (acción de macro)


**Se aplica a:** Access 2013, Office 2013

Puede usar la acción **DetenerTodasMacros** para detener todas las macros actualmente en ejecución.

## <a name="setting"></a>Configuración

La acción **DetenerTodasMacros** no utiliza ningún argumento.

## <a name="remarks"></a>Comentarios

Esta acción se suele utilizar cuando es necesario detener todas las macros debido a un error. Puede usar una expresión condicional en la fila de acción de la macro que contiene esta acción. Cuando la expresión se evalúa como **Verdadero** (–1), Microsoft Access detiene todas las macros.

Por ejemplo, podría disponer de una macro que muestre un cuadro de mensaje como una acción más de una serie de acciones complejas, incluida la ejecución de otras macros. Si el usuario hace clic en **Cancelar** en este cuadro de mensaje, la acción **DetenerTodasMacros** permite detener todas las macros que se están ejecutando.

Si una macro ha utilizado las acciones **Eco** o **EstablecerAdvertencias** para desactivar el eco o la presentación de mensajes del sistema, la acción **DetenerTodasMacros** volverá a activarlos automáticamente.

Esta acción no está disponible en un módulo de Visual Basic para Aplicaciones (VBA).

