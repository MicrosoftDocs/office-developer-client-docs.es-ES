---
title: CerrarBaseDeDatos (acción de macro)
TOCTitle: CloseDatabase Macro Action
ms:assetid: c4b4278d-932c-99f6-da2d-8953109b44b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823085(v=office.15)
ms:contentKeyID: 48547598
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2c60d53b6798d3385bdcfb17669134a04ba6195
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486652"
---
# <a name="closedatabase-macro-action"></a>CerrarBaseDeDatos (acción de macro)


**Se aplica a**: Access 2013 | Office 2013

La acción **CerrarBaseDeDatos** puede usarse para cerrar la actual base de datos.

## <a name="setting"></a>Configuración

La acción **CerrarBaseDeDatos** no tiene ningún argumento.

## <a name="remarks"></a>Comentarios

  - Access no ejecuta ninguna acción que siga a la acción **CerrarBaseDeDatos** de una macro.

  - Esta acción tiene el mismo efecto que hacer clic en la pestaña **archivo** y, a continuación, haciendo clic en **Cerrar base de datos**. Si hay objetos abiertos que no se guardaron cuando ejecuta la acción **CerrarBaseDeDatos**, los cuadros de diálogo que aparecen son los mismos que los que se muestran al hacer clic en **Cerrar base de datos**.

  - Para ejecutar la acción **CerrarBaseDeDatos** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **CloseDatabase** del objeto **DoCmd**.

