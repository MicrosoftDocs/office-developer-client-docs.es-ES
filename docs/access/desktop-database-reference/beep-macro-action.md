---
title: Acción de macro Beep (referencia de escritorio de la base de datos de Access)
TOCTitle: Beep macro action
ms:assetid: 5ca1600f-7934-3b3d-19fd-f305cda0e5d8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194572(v=office.15)
ms:contentKeyID: 48545092
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11853
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 96051d8389f4b8ba7005c75ccdb5e2780ba17138
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721475"
---
# <a name="beep-macro-action"></a>Bip (acción de macro)


**Se aplica a**: Access 2013, Office 2013

La acción **Bip** se puede utilizar para emitir un sonido a través de los altavoces del equipo.

## <a name="setting"></a>Configuración

La acción **Bip** no tiene argumentos.

## <a name="remarks"></a>Comentarios

La acción **Bip** se puede utilizar para indicar las circunstancias siguientes:

  - Se produjeron cambios importantes en la pantalla.

  - Se han especificado datos de un tipo incorrecto en un control. Por ejemplo, si el usuario ha especificado datos numéricos en un control de cuadro de texto.

  - Una macro ha llegado a un punto específico o ha finalizado sus acciones.

La frecuencia y la duración del tono dependen del hardware, que puede ser diferente en cada equipo.

Para ejecutar la acción **Bip** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **Beep** del objeto **DoCmd**.

