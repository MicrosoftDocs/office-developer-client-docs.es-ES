---
title: CerrarBaseDeDatos (acción de macro)
TOCTitle: CloseDatabase macro action
ms:assetid: c4b4278d-932c-99f6-da2d-8953109b44b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823085(v=office.15)
ms:contentKeyID: 48547598
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ac29cbdae8c162a992f2763530514150ca0240ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296300"
---
# <a name="closedatabase-macro-action"></a>CerrarBaseDeDatos (acción de macro)


**Se aplica a:** Access 2013, Office 2013

La acción **CerrarBaseDeDatos** puede usarse para cerrar la actual base de datos.

## <a name="setting"></a>Setting

La acción **CerrarBaseDeDatos** no tiene ningún argumento.

## <a name="remarks"></a>Comentarios

  - Access no ejecuta ninguna acción que siga a la acción **CerrarBaseDeDatos** de una macro.

  - Esta acción tiene el mismo efecto que hacer clic en **la** pestaña Archivo y, a continuación, en Cerrar base **de datos**. Si hay objetos abiertos que no se guardaron cuando ejecuta la acción **CerrarBaseDeDatos**, los cuadros de diálogo que aparecen son los mismos que los que se muestran al hacer clic en **Cerrar base de datos**.

  - Para ejecutar la acción **CerrarBaseDeDatos** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **CloseDatabase** del objeto **DoCmd**.

