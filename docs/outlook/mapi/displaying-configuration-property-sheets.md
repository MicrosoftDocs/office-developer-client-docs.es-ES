---
title: Mostrar hojas de propiedades de configuración
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9386b98-615f-488c-8212-11d9abebbdcf
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a796f458e9d30206dc4c6feb37cbdb1e6b6a704b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421315"
---
# <a name="displaying-configuration-property-sheets"></a>Mostrar hojas de propiedades de configuración

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de transporte usan el método [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) para implementar las hojas de propiedades de configuración. Cuando se llama a **DoConfigPropSheet**, el proveedor de transporte pasa un puntero a una matriz de propiedades junto con información sobre cómo mostrarlos. MAPI a continuación presenta las propiedades al usuario por medio de un cuadro de diálogo estándar. Se recomienda encarecidamente usar este mecanismo de hoja de propiedades al implementar el proveedor de transporte debido a las ventajas que tiene el usuario de una interfaz coherente.
  
## <a name="transport-providers"></a>Proveedores de transporte

Los proveedores de transporte pueden usar la función [BuildDisplayTable](builddisplaytable.md) para simplificar la creación de una tabla de presentación para su uso con **DoConfigPropSheet**. Los proveedores de transporte también pueden usar la API de la hoja de propiedades directamente. Para almacenar en búfer los cambios en las propiedades, los proveedores de transporte pueden usar la función [CreateIProp](createiprop.md) . Esto simplifica el tratamiento de las cancelaciones por parte del usuario mientras el usuario modifica los valores almacenados en las propiedades. Si es necesario, un proveedor de transporte también puede proporcionar un cuadro de diálogo de Asistente para simplificar las tareas de configuración del usuario. 
  

