---
title: Marcado de objetos de negocio como seguros para el scripting
TOCTitle: Marking business objects as safe for scripting
ms:assetid: 8ee49aec-672d-96f7-baa6-9261317a4d90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249630(v=office.15)
ms:contentKeyID: 48546295
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fe5d331b7f3ab4685cb930323076d111a25ec68e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289780"
---
# <a name="marking-business-objects-as-safe-for-scripting"></a>Marcado de objetos de negocio como seguros para el scripting

**Se aplica a:** Access 2013, Office 2013

Para ayudar a garantizar un entorno de Internet seguro, es necesario marcar cualquier instancia de objeto de negocio creada con el método [CreateObject](dataspace-object-rds.md) del objeto [RDS.DataSpace](createobject-method-rds.md) como "segura para scripting". Es necesario garantizar que se marcan de ese modo en el área de Licencia del Registro del sistema antes de que se puedan usar en DCOM.

Para marcar manualmente el objeto de negocio como "seguro para scripting", cree un archivo de texto con extensión .reg que contenga el siguiente texto. Los dos números siguientes habilitan la característica de seguridad para scripting:

```vb 
 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95801-9882-11CF-9FA9-00AA006C42C4}] 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95802-9882-11CF-9FA9-00AA006C42C4}] 
```

donde \< *MyActiveXGUID* \> es el número GUID hexadecimal del objeto de negocio. Guárdelo e insértelo en el Registro mediante el Editor del registro o haciendo doble clic sobre el archivo .reg desde el Explorador de Windows.

Los objetos empresariales creados en Microsoft Visual Basic se pueden marcar automáticamente como "seguros para scripting" con el Asistente para paquetes e implementación. Cuando el asistente le pida que especifique una configuración de seguridad, seleccione **Seguro para inicialización** y **Seguro para scripting**.

En el último paso, el Asistente para la instalación de aplicaciones crea un archivo .htm y un archivo .cab. Puede copiar estos dos archivos en el equipo de destino y hacer a continuación doble clic en el archivo .htm para cargar la página y registrar el servidor correctamente.

Dado que el objeto de negocio se instalará en el directorio de Windows System32 Occache de forma predeterminada, muévelo al directorio de Windows System32 y cambia la clave del Registro \\ \\ \\ **HKEY \_ CLASSES ROOT \_ \\ CLSID \\** \< *MyActiveXGUID* \> \\ **InprocServer32** para que coincida con la ruta de acceso correcta.


> [!NOTE]
> [!NOTA] De los objetos de negocio marcados como seguros para scripting o seguros para inicialización se puede crear una instancia que cualquiera podrá inicializar a través de la red. Ningún objeto de negocio personalizado se debe diseñar e implementar a la ligera. Es fundamental que dichos objetos no representen una amenaza a la seguridad que pueda ser aprovechada por hackers para tener acceso al área confidencial del servidor y causar daños.


