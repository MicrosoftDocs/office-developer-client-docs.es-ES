---
title: Marcar objetos de negocio como seguros para scripting
TOCTitle: Marking Business Objects as Safe for Scripting
ms:assetid: 8ee49aec-672d-96f7-baa6-9261317a4d90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249630(v=office.15)
ms:contentKeyID: 48546295
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7ac928f7e61cf633aac6963565cf3aae441a2ac6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486136"
---
# <a name="marking-business-objects-as-safe-for-scripting"></a><span data-ttu-id="3e2ea-102">Marcar objetos de negocio como seguros para scripting</span><span class="sxs-lookup"><span data-stu-id="3e2ea-102">Marking Business Objects as Safe for Scripting</span></span>


<span data-ttu-id="3e2ea-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3e2ea-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3e2ea-p101">Para ayudar a garantizar un entorno de Internet seguro, es necesario marcar cualquier instancia de objeto de negocio creada con el método [CreateObject](dataspace-object-rds.md) del objeto [RDS.DataSpace](createobject-method-rds.md) como "segura para scripting". Es necesario garantizar que se marcan de ese modo en el área de Licencia del Registro del sistema antes de que se puedan usar en DCOM.</span><span class="sxs-lookup"><span data-stu-id="3e2ea-p101">To help ensure a secure Internet environment, you need to mark any business objects instantiated with the [RDS.DataSpace](dataspace-object-rds.md) object's [CreateObject](createobject-method-rds.md) method as "safe for scripting." You need to ensure they are marked as such in the License area of the system registry before they can be used in DCOM.</span></span>

<span data-ttu-id="3e2ea-p102">Para marcar manualmente el objeto de negocio como "seguro para scripting", cree un archivo de texto con extensión .reg que contenga el siguiente texto. Los dos números siguientes habilitan la característica de seguridad para scripting:</span><span class="sxs-lookup"><span data-stu-id="3e2ea-p102">To manually mark your business object as safe for scripting, create a text file with a .reg extension that contains the following text. The following two numbers enable the safe-for-scripting feature:</span></span>

```vb 
 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95801-9882-11CF-9FA9-00AA006C42C4}] 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95802-9882-11CF-9FA9-00AA006C42C4}] 
```

<span data-ttu-id="3e2ea-108">donde \< *MyActiveXGUID* \> es el número GUID hexadecimal de su objeto de negocio.</span><span class="sxs-lookup"><span data-stu-id="3e2ea-108">where \<*MyActiveXGUID*\> is the hexadecimal GUID number of your business object.</span></span> <span data-ttu-id="3e2ea-109">Guárdelo e insértelo en el Registro mediante el Editor del registro o haciendo doble clic sobre el archivo .reg desde el Explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="3e2ea-109">Save it and merge it into your registry by using the Registry Editor or double-clicking the .reg file in Windows Explorer.</span></span>

<span data-ttu-id="3e2ea-p104">Los objetos de negocio creados en Microsoft® Visual Basic se pueden marcar automáticamente como "seguros para scripting" con el Asistente para empaquetado y distribución. Cuando el asistente le pida que especifique una configuración de seguridad, seleccione **Seguro para inicialización** y **Seguro para scripting**.</span><span class="sxs-lookup"><span data-stu-id="3e2ea-p104">Business objects created in Microsoft® Visual Basic can be automatically marked as "safe for scripting" with the Package and Deployment Wizard. When the wizard asks you to specify safety settings, select **Safe for initialization** and **Safe for scripting**.</span></span>

<span data-ttu-id="3e2ea-p105">En el último paso, el Asistente para la instalación de aplicaciones crea un archivo .htm y un archivo .cab. Puede copiar estos dos archivos en el equipo de destino y hacer a continuación doble clic en el archivo .htm para cargar la página y registrar el servidor correctamente.</span><span class="sxs-lookup"><span data-stu-id="3e2ea-p105">On the last step, the Application Setup Wizard creates an .htm and a .cab file. You can then copy these two files to the target computer and double-click the .htm file to load the page and correctly register the server.</span></span>

<span data-ttu-id="3e2ea-114">Debido a que el objeto de negocio se instalará en el Windows\\System32\\directorio Occache de forma predeterminada, moverlo a las ventanas\\directorio System32 y cambiar la **HKEY\_clases\_raíz\\CLSID\\ \*\* \< *MyActiveXGUID*\>\\**InprocServer32\*\* clave de registro para que coincida con la ruta de acceso correcta.</span><span class="sxs-lookup"><span data-stu-id="3e2ea-114">Because the business object will be installed in the Windows\\System32\\Occache directory by default, move it to the Windows\\System32 directory and change the **HKEY\_CLASSES\_ROOT\\CLSID\\**\<*MyActiveXGUID*\>\\**InprocServer32** registry key to match the correct path.</span></span>


> [!NOTE]
> <span data-ttu-id="3e2ea-p106">[!NOTA] De los objetos de negocio marcados como seguros para scripting o seguros para inicialización se puede crear una instancia que cualquiera podrá inicializar a través de la red. Ningún objeto de negocio personalizado se debe diseñar e implementar a la ligera. Es fundamental que dichos objetos no representen una amenaza a la seguridad que pueda ser aprovechada por hackers para tener acceso al área confidencial del servidor y causar daños.</span><span class="sxs-lookup"><span data-stu-id="3e2ea-p106">Business objects marked as safe for scripting or safe for initialization can be instantiated and initialized by anyone over the network. Any custom business object must not be designed and implemented casually. It is imperative that such objects do not present a security threat that hackers can explore to gain access to the sensitive area of the hosting server and inflict damages.</span></span>

