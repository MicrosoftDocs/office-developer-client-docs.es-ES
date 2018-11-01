---
title: DetenerTodasMacros (acción de macro)
TOCTitle: StopAllMacros Macro Action
ms:assetid: 6afbf906-03b8-6e68-bbc9-7a4b141cf1c5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195440(v=office.15)
ms:contentKeyID: 48545442
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm104968
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4d9452bed9a301c82d32c0c0a0800eb7b29231b0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870516"
---
# <a name="stopallmacros-macro-action"></a>DetenerTodasMacros (acción de macro)


**Se aplica a**: Access 2013, Office 2013

Puede usar la acción **DetenerTodasMacros** para detener todas las macros actualmente en ejecución.

## <a name="setting"></a>Configuración

La acción **DetenerTodasMacros** no utiliza ningún argumento.

## <a name="remarks"></a>Comentarios

Esta acción se suele utilizar cuando es necesario detener todas las macros debido a un error. Puede usar una expresión condicional en la fila de acción de la macro que contiene esta acción. Cuando la expresión se evalúa como **True** (-1), Microsoft Access detiene todas las macros.

Por ejemplo, podría disponer de una macro que muestre un cuadro de mensaje como una acción más de una serie de acciones complejas, incluida la ejecución de otras macros. Si el usuario hace clic en **Cancelar** en este cuadro de mensaje, la acción **DetenerTodasMacros** permite detener todas las macros que se están ejecutando.

Si una macro ha utilizado las acciones **Eco** o **EstablecerAdvertencias** para desactivar el eco o la presentación de mensajes del sistema, la acción **DetenerTodasMacros** volverá a activarlos automáticamente.

Esta acción no está disponible en un módulo de Visual Basic para Aplicaciones (VBA).

