---
title: Instalación del complemento de estado sin conexión de muestra
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Última modificación: 06 de julio de 2012'
ms.openlocfilehash: b7b9ce539537e0759020ef7e3b4f6541a940d6fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317216"
---
# <a name="installing-the-sample-offline-state-add-in"></a>Instalación del complemento de estado sin conexión de muestra

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Este tema le guiará por los pasos necesarios para descargar e instalar el complemento de estado sin conexión de muestra. El complemento de estado sin conexión de muestra es un complemento COM que agrega un menú de **estado sin conexión** a Outlook y usa la API de estado sin conexión. Mediante el menú estado sin conexión, puede habilitar o deshabilitar la supervisión de estado, comprobar el estado actual y cambiar el estado actual. Para obtener más información sobre cómo se implementa el complemento de estado sin conexión, consulte [configurar un complemento de estado sin conexión](setting-up-an-offline-state-add-in.md).
  
## <a name="install-the-sample-offline-state-add-in"></a>Instalar el complemento de estado sin conexión de muestra

1. Descargue el complemento de estado sin conexión de muestra aquí: [ejemplos de código de referencia auxiliar de Outlook 2007 y el instalador](https://www.microsoft.com/en-us/download/details.aspx?id=24102)redistribuible.
    
2. Ejecute Visual Studio 2005 como administrador.
    
    > [!NOTE]
    > Si el equipo ejecuta Windows XP, debe iniciar sesión como administrador. Si el equipo ejecuta Windows Vista, debe iniciar sesión como administrador. Haga clic con el botón secundario en el icono de Visual Studio 2005 y haga clic en **Ejecutar como administrador**. 
  
3. En Visual Studio 2005, haga clic en **archivo**, seleccione **abrir**y, a continuación, haga clic en **proyecto o solución**.
    
4. Vaya a la ubicación en la que guardó el ejemplo, haga clic en **ConnectionStateAddin**y, a continuación, haga clic en **abrir**.
    
5. On the **Build** menu, click **Build Solution**.
    
6. En el cuadro de diálogo **Guardar archivo como** , haga clic en **Guardar**.
    
7. Haga clic en el menú **Inicio** , en **todos los programas**, en **accesorios**, haga clic con el botón secundario en **símbolo del sistema**y, a continuación, haga clic en **Ejecutar como administrador**.
    
    > [!NOTE]
    > Si está ejecutando Windows XP, debe iniciar sesión como administrador. 
  
8. En el cuadro de diálogo **Control de cuentas de usuario**, haga clic en **Continuar**.
    
9. En la ventana del **símbolo del sistema** , cambie los directorios a la carpeta de depuración donde guardó el ejemplo. Por ejemplo, si guardó el ejemplo en el C:\ Escriba **CD "C:\ConnectionStateAddin\Debug"** y, a continuación, presione **entrar**. 
    
10. Escriba **regsvr32 OfflineStateAddin. dll** y presione **entrar**. 
    
    > [!NOTE]
    > Para desinstalar el complemento de estado sin conexión de muestra, escriba **regsvr32-u OfflineStateAddin. dll.**
  
11. En el cuadro de diálogo **RegSrv32** , haga clic en **Aceptar**.
    
12. ReInicie Outlook para ver el menú **estado sin conexión** . 
    
## <a name="see-also"></a>Vea también



[Información sobre la API de estado sin conexión](about-the-offline-state-api.md)
  
[Instalar el complemento de estado sin conexión de muestra](installing-the-sample-offline-state-add-in.md)
  
[Información sobre el complemento de estado sin conexión de muestra](about-the-sample-offline-state-add-in.md)
  
[Configurar un complemento de estado sin conexión](setting-up-an-offline-state-add-in.md)
  
[Supervisar los cambios de estado de conexión con un complemento de estado sin conexión](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[Desconexión de un complemento de estado sin conexión](disconnecting-an-offline-state-add-in.md)

