---
title: Instalación del proveedor de almacén de archivos PST ajustado de ejemplo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90ce0ea3-ba73-cb57-0fa9-8898bc4ac9de
description: '�ltima modificaci�n: jueves, 5 de julio de 2012'
ms.openlocfilehash: a1574de555eb74d06c4dbe721e7e013ac59d3071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309635"
---
# <a name="installing-the-sample-wrapped-pst-store-provider"></a>Instalación del proveedor de almacén de archivos PST ajustado de ejemplo

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Este tema le guiará por los pasos necesarios para descargar e instalar el proveedor de almacén de archivos PST ajustado de ejemplo. El proveedor de almacén de archivos PST ajustado de ejemplo, WrapPST, implementa un proveedor de almacenamiento PST ajustado que está pensado para usarse junto con la API de replicación. Para obtener más información acerca de la API de replicación, consulte [About the replicaTION API](about-the-replication-api.md).
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a>Instalación del proveedor de almacén de archivos PST ajustado de muestra

1. Para descargar el proveedor de almacén de archivos PST ajustado de muestra, vea [ejemplos de código de referencia auxiliar de Outlook 2007 y el instalador](https://www.microsoft.com/en-us/download/details.aspx?id=24102)redistribuible.
    
2. Abra la carpeta **SampleWrappedPSTStoreProvider** y haga clic en **extraer todos los archivos**.
    
3. Haga clic en **examinar**, seleccione la ubicación en la que desea guardar el ejemplo y haga clic en **Aceptar**.
    
4. Haga clic en **Extraer**. La carpeta seleccionada aparecerá y contendrá los archivos extraídos.
    
5. Abra Visual Studio 2005 como administrador.
    
    > [!NOTE]
    > Si el equipo ejecuta Windows XP, debe iniciar sesión como administrador. Si su equipo ejecuta Windows Vista, debe iniciar sesión como administrador y debe hacer clic con el botón secundario en el icono de Visual Studio 2005 y hacer clic en **Ejecutar como administrador**. 
  
6. En Visual Studio 2005, haga clic en **archivo**, seleccione **abrir**y, a continuación, haga clic en **proyecto o solución**.
    
7. Vaya a la ubicación en la que guardó el ejemplo, haga clic en **WrapPST**y, a continuación, haga clic en **abrir**.
    
8. On the **Build** menu, click **Build Solution**.
    
9. En el cuadro de diálogo **Guardar archivo como** , haga clic en **Guardar**.
    
10. En la carpeta donde guardó el ejemplo, haga clic con el botón secundario en el archivo **install. bat** y haga clic en **Ejecutar como administrador**.
    
11. En el cuadro de diálogo **Control de cuentas de usuario**, haga clic en **Continuar**.
    
## <a name="see-also"></a>Vea también



[Información sobre el proveedor de almacén de archivos PST ajustado de ejemplo](about-the-sample-wrapped-pst-store-provider.md)
  
[Inicializar un proveedor de almacén de archivos PST ajustado](initializing-a-wrapped-pst-store-provider.md)
  
[Inicio de sesión en un proveedor de almacén de archivos PST ajustado](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Usar un proveedor de almacén de archivos PST ajustado](using-a-wrapped-pst-store-provider.md)
  
[Apagar un proveedor de almacén de archivos PST ajustado](shutting-down-a-wrapped-pst-store-provider.md)

