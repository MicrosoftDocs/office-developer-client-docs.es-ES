---
title: Acción de Macro Beep (referencia de escritorio de la base de datos de Access)
TOCTitle: Beep Macro Action
ms:assetid: 5ca1600f-7934-3b3d-19fd-f305cda0e5d8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194572(v=office.15)
ms:contentKeyID: 48545092
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11853
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7024734b09544042fa58b8cd95127d8195e5788a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486127"
---
# <a name="beep-macro-action"></a>Bip (acción de macro)


**Se aplica a**: Access 2013 | Office 2013

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

