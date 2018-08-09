---
title: Agregar y crear referencias a ensamblados personalizados
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, using custom assemblies,assemblies [InfoPath 2007], adding custom using InfoPath 2003 object model
localization_priority: Normal
ms.assetid: 20e1f43e-8279-48fc-8f34-16a2729dbc9b
description: Si se agrega una referencia a un ensamblado personalizado en un proyecto de plantilla de formulario con código administrado, el ensamblado se incluye dentro del archivo de plantilla de formulario (.xsn) al compilar y publicar el proyecto.
ms.openlocfilehash: e182930ebe14b6f64d1b90509fe400cc1fb1b26e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815861"
---
# <a name="add-and-reference-custom-assemblies"></a>Agregar y crear referencias a ensamblados personalizados

Si se agrega una referencia a un ensamblado personalizado en un proyecto de plantilla de formulario con código administrado, el ensamblado se incluye dentro del archivo de plantilla de formulario (.xsn) al compilar y publicar el proyecto.
  
## <a name="add-and-reference-a-custom-assembly"></a>Agregar y crear una referencia a un ensamblado personalizado

Para evitar conflictos con la forma en que el sistema de proyecto de InfoPath administra los archivos que se agregan al archivo de plantilla de formulario, no copie ningún ensamblado personalizado al que desee hacer referencia en la carpeta de nivel superior de un proyecto de plantilla de formulario. De manera predeterminada, la ruta de acceso de éste tiene el siguiente formato: < *unidad*  >:\Usuarios\  *nombreDeUsuario*  \Documentos\Proyectos de InfoPath\  *nombreDeProyecto* 
  
Si desea mover ensamblados personalizados a los que hace referencia en la carpeta del proyecto, deberá crear una subcarpeta en un nivel inferior a la carpeta principal del proyecto, copiar los ensamblados personalizados de esa subcarpeta y crear referencias a los mismos. Sin embargo, tenga en cuenta que no es necesario crear una subcarpeta para los ensamblados a los que se hace referencia. Siempre que el ensamblado al que se haga referencia no esté ubicado dentro de la carpeta de nivel superior del proyecto, el sistema de proyectos de InfoPath lo copiará en el archivo de plantilla de formulario (.xsn) cuando el proyecto se compile y publique.
  
### <a name="reference-a-custom-assembly-from-its-default-location"></a>Crear una referencia a un ensamblado personalizado desde su ubicación predeterminada

1. Abra el proyecto de plantilla de formulario en Visual Studio 2012.
    
2. En el menú **Proyecto**, haga clic en **Agregar referencia**.
    
3. Haga clic en la pestaña **Examinar**, busque y especifique el ensamblado y, a continuación, haga clic en **Aceptar** para agregar la referencia. 
    
## <a name="see-also"></a>Vea también

#### <a name="tasks"></a>Tareas

[Crear una plantilla de formulario con código mediante el modelo de objetos de InfoPath 2003](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)

