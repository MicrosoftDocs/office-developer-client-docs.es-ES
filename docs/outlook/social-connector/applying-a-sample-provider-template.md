---
title: Aplicar una plantilla de proveedor de ejemplo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'Las plantillas de proveedor de ejemplo Outlook Social Connector (OSC) proporcionan un marco de trabajo para la implementación de un proveedor de OSC. '
ms.openlocfilehash: 2388da58690e1870434c576bfa68649937156c54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821077"
---
# <a name="applying-a-sample-provider-template"></a>Aplicar una plantilla de proveedor de ejemplo

Las plantillas de proveedor de ejemplo Outlook Social Connector (OSC) proporcionan un marco de trabajo para la implementación de un proveedor de OSC. Las plantillas de proveedor están disponibles en C++, C# y Visual Basic. Estas plantillas son simplemente un punto de partida para el desarrollo de proveedor; las plantillas no responden a escribir el código de implementación para el proveedor y la creación de un paquete de instalación para el proveedor. El siguiente procedimiento muestra cómo aplicar una plantilla de proveedor OSC cuando comience a desarrollar un proveedor.
  
### <a name="to-apply-an-osc-provider-template"></a>Para aplicar una plantilla de proveedor OSC

1. En el menú **Inicio** , haga clic en **Microsoft Visual Studio 2010** y haga clic en el comando **Ejecutar como administrador** . Cuando se le solicite, haga clic en **Sí** para ejecutar Visual Studio como administrador. 
    
2. Cambie el nombre del proyecto y el espacio de nombres en la plantilla a los identificadores de nombre y espacio de nombres de proyecto.
    
3. Modifique la clase **AssemblyInfo** para especificar la información de ensamblado adecuado. 
    
4. Implementar los miembros de interfaz marcados como **tareas pendientes** y agregue más dependencias y referencias, según sea necesario. 
    
5. Genere el proyecto.
    
6. Asegúrese de que el ensamblado del proveedor ProgID aparece como una clave en `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.
    
7. Para distribuir el proyecto de instalación, cree un proyecto de instalación en Visual Studio o una herramienta de configuración de su elección.
    
8. El proyecto de instalación debe completar el registro de COM para el ensamblado y también crear la clave ProgID que se enumeran en el paso 5.
    
## <a name="see-also"></a>Vea también

- [Descarga de los ejemplos de](downloading-the-samples.md)
- [Plantillas de ejemplo OSC](osc-sample-templates.md)

