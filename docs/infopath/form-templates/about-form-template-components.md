---
title: Acerca de los componentes de las plantillas de formulario
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: b51361fe-cf29-f890-9876-5aebe15c73e1
description: Las plantillas de formulario de Microsoft InfoPath se componen de varios archivos y componentes que se combinan para proporcionar funcionalidad específica para escenarios de usuario final o necesidades empresariales concretos. La complejidad de los formularios de InfoPath varía en función del tipo de necesidad que abordan.
ms.openlocfilehash: 4ef90d3fb55ee38018d2c1226bef5fd59e277186
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815849"
---
# <a name="about-form-template-components"></a>Acerca de los componentes de las plantillas de formulario

Las plantillas de formulario de Microsoft InfoPath se componen de varios archivos y componentes que se combinan para proporcionar funcionalidad específica para escenarios de usuario final o necesidades empresariales concretos. La complejidad de los formularios de InfoPath varía en función del tipo de necesidad que abordan.
  
Una plantilla de formulario de InfoPath es, básicamente, un tipo de aplicación que crea una clase específica de documentos XML, define su diseño y comportamiento de edición, asegura la coherencia de sus datos y ofrece la información de enrutamiento que indica dónde deben almacenarse.
  
Es importante comprender que las plantillas de formulario de InfoPath se componen de varios archivos distintos, que se denominan colectivamente archivos de formulario. En general, una plantilla de formulario de InfoPath se compone de los siguientes tipos de archivos.
  
|**Name**|**Extension**|**Descripción**|
|:-----|:-----|:-----|
|Definición del formulario  <br/> |.xsf  <br/> |Archivo generado por InfoPath que contiene información sobre los demás archivos y componentes usados en un formulario. Este archivo actúa como manifiesto del formulario.  <br/> |
|Esquema XML  <br/> |.xsd  <br/> |Archivos del esquema XML que se usan para restringir y validar los archivos de documento XML subyacentes del formulario.  <br/> |
|Vista  <br/> |.xsl  <br/> |Archivos de presentación lógica usados para presentar, ver y transformar los datos contenidos en los archivos de documento XML subyacentes del formulario.  <br/> |
|Plantilla XML  <br/> |.Xml  <br/> |Archivo .xml que contiene los datos predeterminados que se muestran en una vista cuando se crea un nuevo formulario.  <br/> |
|Presentación  <br/> |.htm, .gif, .bmp y otros  <br/> |Archivos que se usan junto con los archivos de vista para crear una interfaz de usuario personalizada.  <br/> |
|Lógica empresarial  <br/> |.dll  <br/> |Código de programación compilado que se usa para implementar el comportamiento de edición específico, la validación de datos, los controladores de eventos, el flujo de control de datos y más lógica empresarial personalizada. La lógica empresarial de InfoPath se puede escribir en los lenguajes de programación Visual Basic y C# .NET, que están compilados e incluidos como archivos binarios.  <br/> |
|Binario  <br/> |.dll, .exe  <br/> | Todo componente personalizado que proporcione lógica empresarial adicional.  <br/> |
|Plantilla de formulario  <br/> |.xsn  <br/> |Formato de archivo comprimido (.cab) que empaqueta todos los archivos de formulario en un archivo.  <br/> |
   

