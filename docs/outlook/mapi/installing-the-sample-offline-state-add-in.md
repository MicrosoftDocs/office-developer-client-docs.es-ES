---
title: Instalar el complemento de estado sin conexión de muestra
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Última modificación: 06 de julio de 2012'
ms.openlocfilehash: 00232f290c367c4bab1854bfe3909abc7b03cef8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817846"
---
# <a name="installing-the-sample-offline-state-add-in"></a>Instalar el complemento de estado sin conexión de muestra

  
  
**Hace referencia a**: Outlook 
  
En este tema le lleva a través de los pasos para descargar e instalar el complemento de estado sin conexión de ejemplo. El complemento de estado sin conexión de ejemplo es un complemento COM que se agrega un menú de **Estado desconectado** a Outlook y utiliza la API de estado sin conexión. A través del menú de estado sin conexión se puede habilitar o deshabilitar la supervisión de estado, compruebe el estado actual y cambiar el estado actual. Para obtener más información acerca de cómo se implementa el complemento de estado sin conexión, vea [Agregar en configuración de seguridad de un estado no conectado](setting-up-an-offline-state-add-in.md).
  
## <a name="install-the-sample-offline-state-add-in"></a>Instalar el ejemplo sin conexión estado Add-in

1. Descargue el ejemplo desconectado estado complemento aquí: [ejemplos de código de referencia auxiliar de Outlook 2007 e instalador redistribuible](http://www.microsoft.com/en-us/download/details.aspx?id=24102).
    
2. Ejecute Visual Studio 2005 como administrador.
    
    > [!NOTE]
    > Si su equipo está ejecutando Windows XP, debe haber iniciado sesión como administrador. Si su equipo ejecuta Windows Vista, debe haber iniciado sesión como administrador. Haga clic en el icono de Visual Studio 2005 y haga clic en **Ejecutar como administrador**. 
  
3. En Visual Studio 2005, haga clic en **archivo**, seleccione **Abrir**y, a continuación, haga clic en **Proyecto o solución**.
    
4. Vaya a la ubicación donde guardó el ejemplo, haga clic en **ConnectionStateAddin**y, a continuación, haga clic en **Abrir**.
    
5. On the **Build** menu, click **Build Solution**.
    
6. En el cuadro de diálogo **Guardar archivo como** , haga clic en **Guardar**.
    
7. Haga clic en el menú **Inicio** , haga clic en **Todos los programas**, haga clic en **Accesorios**, haga clic en **el símbolo del sistema**y, a continuación, haga clic en **Ejecutar como administrador**.
    
    > [!NOTE]
    > Si está ejecutando Windows XP, debe haber iniciado sesión como administrador. 
  
8. En el cuadro de diálogo **Control de cuentas de usuario** , haga clic en **continuar**.
    
9. En la ventana de **símbolo del sistema** , cambie los directorios a la carpeta de depuración donde guardó el ejemplo. Por ejemplo, si guardó el ejemplo en la unidad C:\, escriba **cd "C:\ConnectionStateAddin\Debug"** y, a continuación, presione **ENTRAR**. 
    
10. Escriba **regsvr32 OfflineStateAddin.dll** y presione **ENTRAR**. 
    
    > [!NOTE]
    > Para desinstalar el complemento de estado de ejemplo sin conexión, escriba **regsvr32 -u OfflineStateAddin.dll**
  
11. En el cuadro de diálogo **RegSrv32** , haga clic en **Aceptar**.
    
12. Reinicie Outlook para ver el menú de **Estado sin conexión** . 
    
## <a name="see-also"></a>Vea también



[Información sobre la API de estado sin conexión](about-the-offline-state-api.md)
  
[Instalar el complemento de estado sin conexión de muestra](installing-the-sample-offline-state-add-in.md)
  
[Información sobre el complemento de estado sin conexión de muestra](about-the-sample-offline-state-add-in.md)
  
[Configurar un complemento de estado sin conexión](setting-up-an-offline-state-add-in.md)
  
[Supervisar los cambios estado de conexión con un complemento de estado sin conexión](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[Desconectar un complemento de estado sin conexión](disconnecting-an-offline-state-add-in.md)

