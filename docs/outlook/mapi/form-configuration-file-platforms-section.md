---
title: Sección del archivo de configuración de formulario [Plataformas]
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d86edfb6fcc72c5968a8ff5d9cd739e20e5dec43
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589899"
---
# <a name="form-configuration-file-platforms-section"></a>Sección del archivo de configuración de formulario [Plataformas]

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La sección **[plataformas]** enumera el conjunto completo de plataformas compatibles con este formulario. Cada entrada de plataforma consta del prefijo **plataforma.** _cadena_, donde la _cadena_ es un código de cadena arbitraria para la plataforma Cada cadena corresponde a la entrada de **CPU** de un secciones **[plataformas]** individuales. Cada entrada en una sección **[plataformas]** define una _cadena de la plataforma_ que hace referencia a una posterior **[plataforma.** _cadena de plataforma_ sección de **]** tal como se muestra aquí. 
  
La sección **[plataformas]** enumera el conjunto completo de plataformas compatibles con este formulario. Cada entrada de plataforma consta del prefijo **plataforma.** _cadena_, donde la _cadena_ es un código de cadena arbitraria para la plataforma Cada cadena corresponde a la entrada de **CPU** de un secciones **[plataformas]** individuales. Cada entrada en una sección **[plataformas]** define una _cadena de la plataforma_ que hace referencia a una posterior **[plataforma.** _cadena de plataforma_ sección de **]** tal como se muestra aquí. 
  
**[Plataformas]**
  
**Plataforma**. _cadena_ =  _cadena de plataforma_
  
Siguiente es un ejemplo de una sección **[plataformas]** . 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

Cada **[plataforma.** _cadena de plataforma_ sección **]** contiene las dos entradas necesarias, **CPU** y **OSVersion**. La entrada de **CPU** especifica el procesador, y la entrada **OSVersion** especifica el sistema operativo. Los valores válidos de **CPU** se describen en la siguiente tabla. 
  
|**Entrada de CPU**|**Procesador**|
|:-----|:-----|
|Ix86  <br/> |Intel 80 x 86 y procesadores Pentium de la serie, así como los procesadores equivalentes de AMD, Cyrix, NextGen y otros fabricantes.  <br/> |
|MIPS  <br/> |Procesadores de la serie de MIPS R4000.  <br/> |
|AXP  <br/> |Procesador Digital Equipment Corporation Alpha AXP.  <br/> |
|PPC  <br/> |Procesadores de la serie de Motorola Power PC.  <br/> |
|M68  <br/> |Procesadores de la serie Mororola 68 x 00.  <br/> |
   
Los valores válidos de **OSVersion** se describen en la siguiente tabla. 
  
|**Entrada de OSVersion**|**Sistema operativo**|
|:-----|:-----|
|Win3.1  <br/> |Windows 3.1 y Windows para trabajo en grupo 3.11.  <br/> |
|WinNT3.5  <br/> |Windows NT 3.5 o inferior.  <br/> |
|Windows 95  <br/> |Windows 95.  <br/> |
|WinNT4.0  <br/> |Windows NT 4.0.  <br/> |
|Mac7  <br/> |Sistema de Macintosh 7.  <br/> |
   
Además, el **[plataforma.** _cadena de plataforma_ sección **]** debe contener una entrada de un **archivo** o **enlacesa** . La entrada de **archivo** enumera el archivo ejecutable de aplicación de servidor de formulario que mantiene la biblioteca de formularios y se carga en un subdirectorio nuevo en la caché de disco cuando se inicia el formulario. Si una entrada **enlacesa** se usa en su lugar, contiene el nombre de una cadena de plataforma diferente de la que se toma la información del **archivo** . Esto es útil si una versión de un formulario es compatible con varias plataformas. 
  
La entrada **del registro** se usa siempre que se utiliza la entrada de **archivo** , identifica la clave del registro de la biblioteca de formularios donde se almacena el archivo ejecutable de la aplicación de servidor del formulario. Cadenas precedidas por una barra diagonal inversa (\) se colocan en la raíz del registro. Las cadenas no precedidas por una barra diagonal inversa se colocan en el _GUID_de HKEY_CLASSES_ROOT\CLSID\ \ clave del registro, donde _GUID_ es el **GUID** del formulario. Los caracteres "%d" pueden utilizarse para indicar la ruta de acceso del directorio desde el que se ha leído el archivo de configuración del formulario. Esto es útil para especificar otros archivos con nombres de ruta de acceso relativa al archivo de configuración del formulario. Las entradas de **registro** o **Varios archivos** se pueden especificar mediante el uso del registro o archivo como un prefijo seguido de cualquier otro texto. El formato para el **[plataforma.** _cadena de plataforma_ sección **]** es: 
  
- **[Plataforma.** _cadena de plataforma_ **]**
    
- **CPU** =  _cadena_
    
- **OSVersion** =  _cadena_
    
- **Archivo** =  _ruta de acceso_
    
- **Enlacesa** =  _cadena_
    
- **El registro** =  _cadena_
  
Los siguientes son dos ejemplo **[plataforma.** _cadena de plataforma_ en las secciones **]** , uno con la entrada del **archivo** y uno con la entrada **enlacesa** . 
  
```cpp
[Platform.NTx86]
CPU = ix86
OSVersion = WinNT3.5
File = \helpdesk.exe
Registry = Local Server = %d\helpdesk.exe
[Platform.Win95]
CPU = ix86
OSVersion = Win95
LinkTo = NTx86

```

El **[plataforma.** _cadena de plataforma_ sección **]** se omite cuando se agrega un formulario a la biblioteca de formularios local, cuando se supone que el programa de instalación colocó los archivos que constituyen el controlador de clase de mensaje a un almacenamiento local disponible como con nombre en la sección del controlador en el registro OLE y ha realizado el registro OLE en el registro del sistema. 
  

