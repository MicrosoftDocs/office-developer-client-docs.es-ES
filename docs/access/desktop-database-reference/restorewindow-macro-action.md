---
title: RestaurarVentana (acción de macro)
TOCTitle: RestoreWindow macro action
ms:assetid: 507a6452-2be0-a523-1201-0108d2b9d23c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193815(v=office.15)
ms:contentKeyID: 48544796
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11103
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 35637781035b7a449ba574cf5f6c84f2cb5223db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306590"
---
# <a name="restorewindow-macro-action"></a>RestaurarVentana (acción de macro)

**Se aplica a:** Access 2013, Office 2013

Puede usar la acción **RestaurarVentana** para restaurar el tamaño que tenía anteriormente una ventana maximizada o minimizada.

> [!NOTE]
> [!NOTA] Esta acción no puede aplicarse a las ventanas de código en el Editor de Visual Basic. Para obtener información sobre cómo afectar a las ventanas de código, vea el tema de la propiedad **WindowState**.

## <a name="setting"></a>Configuración

La acción **RestaurarVentana** no tiene argumentos.

## <a name="remarks"></a>Comentarios

Esta acción funciona en el objeto seleccionado. Si se ha minimizado un objeto, primero puede seleccionarlo con la acción **SeleccionarObjeto** y, a continuación, restaurar su tamaño anterior mediante la acción **RestaurarVentana**.

Se puede usar la acción **MoverYCambiarTamañoDeVentana** para mover o cambiar el tamaño de una ventana restaurada.

La acción **RestaurarVentana** tiene el mismo efecto que hacer clic en el botón **Restaurar** situado en la esquina superior derecha de la ventana o hacer clic en el comando **Restaurar** del menú **Control** de la ventana.

Para ejecutar la acción **RestaurarVentana** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **Restore** del objeto **DoCmd**.

