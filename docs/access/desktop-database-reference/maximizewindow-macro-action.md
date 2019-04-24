---
title: MaximizarVentana (acción de macro)
TOCTitle: MaximizeWindow macro action
ms:assetid: 79c9e430-07a7-02b2-ff5a-c6b9ec32c5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196171(v=office.15)
ms:contentKeyID: 48545778
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm196948
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 262e6781b61018cec3d52dbb930f380d3ff5bd85
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289752"
---
# <a name="maximizewindow-macro-action"></a>MaximizarVentana (acción de macro)

**Se aplica a:** Access 2013, Office 2013

Si el acceso está configurado para usar ventanas superpuestas en lugar de documentos con fichas, puede usar la acción **maximizarventana** para ampliar la ventana activa de forma que rellene la ventana de Access. Esta acción permite ver el máximo posible del objeto en la ventana activa.

> [!NOTE]
> [!NOTA] Esta acción no puede aplicarse a las ventanas de código en el Editor de Visual Basic. Para obtener información sobre cómo afectar a las ventanas de código, vea el tema de la propiedad **WindowState**.

## <a name="setting"></a>Configuración

La acción **MaximizarVentana** no tiene argumentos.

## <a name="remarks"></a>Comentarios

Esta acción tiene el mismo efecto que hacer clic en el botón **Maximizar** situado en la esquina superior derecha de la ventana o hacer clic en **Maximizar** en el menú **Control** de la ventana.

Se puede utilizar la acción **RestaurarVentana** para restaurar el tamaño que tenía anteriormente una ventana maximizada.

> [!TIP]
> - Si la ventana que desea maximizar no es la ventana activa, puede que sea necesario utilizar la acción **SeleccionarObjeto**.
> - Si se maximiza una ventana en Access, las demás ventanas también se maximizarán al abrirlas o al cambiar a ellas. Sin embargo, los formularios emergentes no se maximizarán. Si desea que un formulario mantenga su tamaño cuando maximice otras ventanas, establezca el valor de la propiedad **Emergente** en **Sí**.

Para ejecutar la acción **MaximizarVentana** desde un módulo de Visual Basic para Aplicaciones, use el método **Maximize** del objeto **DoCmd**.

