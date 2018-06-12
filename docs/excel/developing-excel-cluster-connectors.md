---
title: Desarrollo de conectores de clúster de Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8c9a166ac06685c0a450e1e0bd60b2fbef67d336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815517"
---
# <a name="developing-excel-cluster-connectors"></a>Desarrollo de conectores de clúster de Excel

**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Conectores de clúster de Excel proporcionan un medio para descarga automáticamente las llamadas de función definida por el usuario con seguridad de clúster en un XLL a un servidor de clúster. Para obtener una descripción de las funciones definidas por el usuario de seguras de clúster, vea [Funciones seguras de clúster](cluster-safe-functions.md). Esta descarga puede mejorar el rendimiento mediante la habilitación de más recursos informáticos que se usará. Un conector de clúster normalmente está desarrollado por un proveedor de clúster de cálculo de alto rendimiento.
  
## <a name="cluster-connectors"></a>Conectores de clúster

Un conector de clúster es un archivo DLL que proporciona puntos de entrada definido que Excel utiliza para coordinar las llamadas de función definida por el usuario con seguridad de clúster. Sirve como una interfaz entre Excel y el clúster de cálculo de alto rendimiento, para la sesión de administración, para hacer que la función se llama (pasando el nombre de función completo y argumentos reales de la llamada) y para devolver los resultados de la llamada a Excel a través de una mecanismo de devolución de llamada.
  
Para crear un conector de clúster, cree un archivo DLL que expone los puntos de entrada que aparecen en las [Funciones de conector de clúster de Excel](excel-cluster-connector-functions.md).
  
## <a name="installing-a-cluster-connector"></a>Instalar un conector de clúster

Para hacer que un conector de clúster disponibles en Excel, el código del programa de instalación del conector debe instalar el archivo DLL del conector en el equipo donde está instalado Excel. Además, el código del programa de instalación del conector debe agregar una entrada para el conector en la siguiente clave del registro:
  
Connectors\ de clúster HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel
  
Agregar un nodo a esta clave para el conector de clúster que especifica las siguientes cadenas:
  
-  `Name`: el nombre que aparecerá en la lista de conectores de clúster en Excel.
    
-  `Filename`: la ruta de acceso completa para el archivo DLL.
    

