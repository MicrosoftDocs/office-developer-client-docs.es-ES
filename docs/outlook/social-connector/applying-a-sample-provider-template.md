---
title: Aplicación de una plantilla de proveedor de ejemplo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'Las plantillas de Outlook de proveedor de Social Connector (OSC) de ejemplo le dan un marco para implementar un proveedor de OSC. '
ms.openlocfilehash: 10fb21ab640e298bc655b8cad554fae789e2ad47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425914"
---
# <a name="applying-a-sample-provider-template"></a>Aplicación de una plantilla de proveedor de ejemplo

Las plantillas de Outlook de proveedor de Social Connector (OSC) de ejemplo le dan un marco para implementar un proveedor de OSC. Las plantillas de proveedor están disponibles en C++, C# y Visual Basic. Estas plantillas son solo un punto de partida para el desarrollo del proveedor; las plantillas no abordan la escritura del código de implementación para el proveedor y la creación de un paquete de instalación para el proveedor. El siguiente procedimiento muestra cómo aplicar una plantilla de proveedor de OSC cuando comience a desarrollar un proveedor.
  
### <a name="to-apply-an-osc-provider-template"></a>Para aplicar una plantilla de proveedor de OSC

1. En el **menú Inicio,** haga clic con el **Microsoft Visual Studio 2010** y haga clic **en el comando Ejecutar como** administrador. Cuando se le pida, **haga clic en Sí** para Visual Studio como administrador. 
    
2. Cambie el nombre del proyecto y el espacio de nombres de la plantilla por el nombre del proyecto y los identificadores de espacio de nombres.
    
3. Modifique la **clase AssemblyInfo** para especificar la información de ensamblado adecuada. 
    
4. Implemente los miembros de la **interfaz marcados como To-Do** y agregue más dependencias y referencias, según sea necesario. 
    
5. Cree el proyecto.
    
6. Asegúrese de que el ensamblado del proveedor ProgID aparece como una clave en  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` .
    
7. Para distribuir el proyecto de instalación, cree un proyecto de instalación en Visual Studio o una herramienta de configuración de su elección.
    
8. El proyecto de instalación debe completar el registro COM para el ensamblado y también crear la clave ProgID como se muestra en el paso 5.
    
## <a name="see-also"></a>Vea también

- [Descargar los ejemplos](downloading-the-samples.md)
- [Plantillas de ejemplo de OSC](osc-sample-templates.md)

