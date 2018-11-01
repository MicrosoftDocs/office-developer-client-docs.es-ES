---
title: Workspace.CreateDatabase Method (DAO)
TOCTitle: CreateDatabase Method
ms:assetid: c0ad986e-3b4d-f781-f782-5aa3cdccea7d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822832(v=office.15)
ms:contentKeyID: 48547514
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2ad3d44d67efb240cb97a5b4716e9e00a6951045
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875626"
---
# <a name="workspacecreatedatabase-method-dao"></a><span data-ttu-id="8f74a-102">Workspace.CreateDatabase Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="8f74a-102">Workspace.CreateDatabase Method (DAO)</span></span>


<span data-ttu-id="8f74a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8f74a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8f74a-104">Crea un nuevo objeto **[Database](database-object-dao.md)**, guarda la base de datos en el disco y devuelve un objeto **Database** abierto (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="8f74a-104">Creates a new **[Database](database-object-dao.md)** object, saves the database to disk, and returns an opened **Database** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="8f74a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f74a-105">Syntax</span></span>

<span data-ttu-id="8f74a-106">*expresión* . CreateDatabase (***nombre***, ***Conectar***, ***opción***)</span><span class="sxs-lookup"><span data-stu-id="8f74a-106">*expression* .CreateDatabase(***Name***, ***Connect***, ***Option***)</span></span>

<span data-ttu-id="8f74a-107">*expresión* Variable que representa un objeto **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="8f74a-107">*expression* A variable that represents a **Workspace** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="8f74a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f74a-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8f74a-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="8f74a-109">Name</span></span></p></th>
<th><p><span data-ttu-id="8f74a-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="8f74a-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="8f74a-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8f74a-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="8f74a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f74a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f74a-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="8f74a-113">Name</span></span></p></td>
<td><p><span data-ttu-id="8f74a-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="8f74a-114">Required</span></span></p></td>
<td><p><span data-ttu-id="8f74a-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-116">Cadena de hasta 255 caracteres de longitud que es el nombre del archivo de base de datos que está creando.</span><span class="sxs-lookup"><span data-stu-id="8f74a-116">A String up to 255 characters long that is the name of the database file that you're creating.</span></span> <span data-ttu-id="8f74a-117">Puede ser el nombre de archivo y ruta de acceso completo.</span><span class="sxs-lookup"><span data-stu-id="8f74a-117">It can be the full path and file name.</span></span> <span data-ttu-id="8f74a-118">Si la red lo admite, también puede especificar una ruta de acceso de red, tales como &quot; \\server1\share1\dir1\db1&quot;.</span><span class="sxs-lookup"><span data-stu-id="8f74a-118">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1&quot;.</span></span> <span data-ttu-id="8f74a-119">Sólo se pueden crear archivos de base de datos de Microsoft Access con este método.</span><span class="sxs-lookup"><span data-stu-id="8f74a-119">You can only create Microsoft Access database files with this method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f74a-120">Conexión</span><span class="sxs-lookup"><span data-stu-id="8f74a-120">Connect</span></span></p></td>
<td><p><span data-ttu-id="8f74a-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="8f74a-121">Required</span></span></p></td>
<td><p><span data-ttu-id="8f74a-122"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-122"><strong>String</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="8f74a-p102">Expresión de cadena que especifica un orden de intercalación para crear la base de datos, tal como se especifica en la sección de configuración. Debe proporcionar este argumento o se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="8f74a-p102">A string expression that specifies a collating order for creating the database, as specified in Settings. You must supply this argument or an error occurs.</span></span></p></li>
<li><p><span data-ttu-id="8f74a-125">También puede crear una contraseña para el nuevo objeto <strong>Database</strong> concatenando la cadena de contraseña (comenzando por &quot;; pwd =&quot;) con una constante en el argumento de <em>Configuración regional</em> , como la siguiente:</span><span class="sxs-lookup"><span data-stu-id="8f74a-125">You can also create a password for the new <strong>Database</strong> object by concatenating the password string (starting with &quot;;pwd=&quot;) with a constant in the <em>locale</em> argument, like this:</span></span></p></li>
<li><p><span data-ttu-id="8f74a-126">dbLangSpanish &amp; &quot;; pwd = NuevaContraseña&quot;</span><span class="sxs-lookup"><span data-stu-id="8f74a-126">dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="8f74a-127">Si desea utilizar el argumento <em>locale</em> predeterminado, pero especificar una contraseña, sólo tiene que agregar una cadena de contraseña al argumento <em>locale</em>:</span><span class="sxs-lookup"><span data-stu-id="8f74a-127">If you want to use the default <em>locale</em>, but specify a password, simply enter a password string for the <em>locale</em> argument:</span></span></p></li>
<li><p><span data-ttu-id="8f74a-128">&quot;; pwd = NuevaContraseña&quot;</span><span class="sxs-lookup"><span data-stu-id="8f74a-128">&quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="8f74a-p103">[!NOTA] Use contraseñas seguras que combinen letras mayúsculas y minúsculas, números y símbolos. Las contraseñas que no son seguras no contienen una combinación de estos elementos. Contraseña segura: Y6dh!et5. Contraseña no segura: House27. Use una contraseña segura que pueda recordar para no tener que anotarla.</span><span class="sxs-lookup"><span data-stu-id="8f74a-p103">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f74a-134">Opción</span><span class="sxs-lookup"><span data-stu-id="8f74a-134">Option</span></span></p></td>
<td><p><span data-ttu-id="8f74a-135">Opcional</span><span class="sxs-lookup"><span data-stu-id="8f74a-135">Optional</span></span></p></td>
<td><p><span data-ttu-id="8f74a-136"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-136"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-p104">Constante o combinación de constantes que indican una o varias opciones, tal como se especifica en la sección de configuración. Puede combinar opciones sumando las constantes correspondientes.</span><span class="sxs-lookup"><span data-stu-id="8f74a-p104">A constant or combination of constants that indicates one or more options, as specified in Settings. You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8f74a-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f74a-139">Remarks</span></span>

<span data-ttu-id="8f74a-140">Puede utilizar alguna de las constantes siguientes para el argumento locale si desea especificar la propiedad [CollatingOrder](database-collatingorder-property-dao.md) de texto para comparaciones de cadenas.</span><span class="sxs-lookup"><span data-stu-id="8f74a-140">You can use one of the following constants for the locale argument to specify the [CollatingOrder](database-collatingorder-property-dao.md) property of text for string comparisons.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8f74a-141">Constante</span><span class="sxs-lookup"><span data-stu-id="8f74a-141">Constant</span></span></p></th>
<th><p><span data-ttu-id="8f74a-142">Orden de intercalación</span><span class="sxs-lookup"><span data-stu-id="8f74a-142">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f74a-143"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-143"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-144">Inglés, alemán, francés, portugués, italiano y español (alfab. internacional)</span><span class="sxs-lookup"><span data-stu-id="8f74a-144">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f74a-145"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-145"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-146">Árabe</span><span class="sxs-lookup"><span data-stu-id="8f74a-146">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f74a-147"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-147"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-148">Chino simplificado</span><span class="sxs-lookup"><span data-stu-id="8f74a-148">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f74a-149"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-149"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-150">Chino tradicional</span><span class="sxs-lookup"><span data-stu-id="8f74a-150">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f74a-151"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-151"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-152">Ruso</span><span class="sxs-lookup"><span data-stu-id="8f74a-152">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f74a-153"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-153"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-154">Checo</span><span class="sxs-lookup"><span data-stu-id="8f74a-154">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f74a-155"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-155"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-156">Neerlandés</span><span class="sxs-lookup"><span data-stu-id="8f74a-156">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f74a-157"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-157"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-158">Griego</span><span class="sxs-lookup"><span data-stu-id="8f74a-158">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f74a-159"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-159"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-160">Hebreo</span><span class="sxs-lookup"><span data-stu-id="8f74a-160">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f74a-161"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-161"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-162">Húngaro</span><span class="sxs-lookup"><span data-stu-id="8f74a-162">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f74a-163"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-163"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-164">Islandés</span><span class="sxs-lookup"><span data-stu-id="8f74a-164">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f74a-165"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-165"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-166">Japonés</span><span class="sxs-lookup"><span data-stu-id="8f74a-166">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f74a-167"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-167"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-168">Coreano</span><span class="sxs-lookup"><span data-stu-id="8f74a-168">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f74a-169"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-169"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-170">Idiomas nórdicos (sólo en la versión 1.0 del motor de base de datos de Microsoft Jet)</span><span class="sxs-lookup"><span data-stu-id="8f74a-170">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f74a-171"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-171"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-172">Noruego y danés</span><span class="sxs-lookup"><span data-stu-id="8f74a-172">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f74a-173"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-173"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-174">Polaco</span><span class="sxs-lookup"><span data-stu-id="8f74a-174">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f74a-175"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-175"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-176">Esloveno</span><span class="sxs-lookup"><span data-stu-id="8f74a-176">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f74a-177"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-177"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-178">Español (alfab. tradicional)</span><span class="sxs-lookup"><span data-stu-id="8f74a-178">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f74a-179"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-179"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-180">Sueco y finés</span><span class="sxs-lookup"><span data-stu-id="8f74a-180">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f74a-181"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-181"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-182">Tailandés</span><span class="sxs-lookup"><span data-stu-id="8f74a-182">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f74a-183"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-183"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-184">Turco</span><span class="sxs-lookup"><span data-stu-id="8f74a-184">Turkish</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8f74a-185">Puede utilizar una o varias de las constantes siguientes en el argumento options para especificar la versión que debe tener el formato de datos y si va a cifrar o no la base de datos.</span><span class="sxs-lookup"><span data-stu-id="8f74a-185">You can use one or more of the following constants in the options argument to specify which version the data format should have and whether or not to encrypt the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8f74a-186">Constante</span><span class="sxs-lookup"><span data-stu-id="8f74a-186">Constant</span></span></p></th>
<th><p><span data-ttu-id="8f74a-187">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f74a-187">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f74a-188"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-188"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-189">Crea una base de datos cifrada.</span><span class="sxs-lookup"><span data-stu-id="8f74a-189">Creates an encrypted database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f74a-190"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-190"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-191">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 1.0.</span><span class="sxs-lookup"><span data-stu-id="8f74a-191">Creates a database that uses the Microsoft Jet database engine version 1.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f74a-192"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-192"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-193">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 1.1.</span><span class="sxs-lookup"><span data-stu-id="8f74a-193">Creates a database that uses the Microsoft Jet database engine version 1.1 file format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f74a-194"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-194"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-195">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 2.0.</span><span class="sxs-lookup"><span data-stu-id="8f74a-195">Creates a database that uses the Microsoft Jet database engine version 2.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f74a-196"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-196"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-197">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 3.0 (compatible con la versión 3.5).</span><span class="sxs-lookup"><span data-stu-id="8f74a-197">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f74a-198"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-198"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-199">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 4.0.</span><span class="sxs-lookup"><span data-stu-id="8f74a-199">Creates a database that uses the Microsoft Jet database engine version 4.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f74a-200"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="8f74a-200"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="8f74a-201">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Access versión 12.0.</span><span class="sxs-lookup"><span data-stu-id="8f74a-201">Creates a database that uses the Microsoft Access database engine version 12.0 file format.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8f74a-202">Si omite la constante de cifrado, **CreateDatabase** crea una base de datos no cifrada.</span><span class="sxs-lookup"><span data-stu-id="8f74a-202">If you omit the encryption constant, **CreateDatabase** creates an un-encrypted database.</span></span>

<span data-ttu-id="8f74a-p105">Utilice el método **CreateDatabase** para crear y abrir una base de datos nueva y vacía, y devolver el objeto **Database**. Debe completar su estructura y contenido mediante objetos DAO adicionales. Si desea realizar una copia parcial o completa de una base de datos existente, puede utilizar el método **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** para realizar una copia que puede personalizar.</span><span class="sxs-lookup"><span data-stu-id="8f74a-p105">Use the **CreateDatabase** method to create and open a new, empty database, and return the **Database** object. You must complete its structure and content by using additional DAO objects. If you want to make a partial or complete copy of an existing database, you can use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method to make a copy that you can customize.</span></span>

## <a name="example"></a><span data-ttu-id="8f74a-206">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8f74a-206">Example</span></span>

<span data-ttu-id="8f74a-207">En este ejemplo se utiliza **CreateDatabase** para crear un objeto **Database** nuevo y cifrado.</span><span class="sxs-lookup"><span data-stu-id="8f74a-207">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

```vb
    Sub CreateDatabaseX() 
     
       Dim wrkDefault As Workspace 
       Dim dbsNew As DATABASE 
       Dim prpLoop As Property 
     
       ' Get default Workspace. 
       Set wrkDefault = DBEngine.Workspaces(0) 
     
       ' Make sure there isn't already a file with the name of  
       ' the new database. 
       If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
     
       ' Create a new encrypted database with the specified  
       ' collating order. 
       Set dbsNew = wrkDefault.CreateDatabase("NewDB.mdb", _ 
          dbLangGeneral, dbEncrypt) 
     
       With dbsNew 
          Debug.Print "Properties of " & .Name 
          ' Enumerate the Properties collection of the new  
          ' Database object. 
          For Each prpLoop In .Properties 
             If prpLoop <> "" Then Debug.Print "  " & _ 
                prpLoop.Name & " = " & prpLoop 
          Next prpLoop 
       End With 
     
       dbsNew.Close 
     
    End Sub
```
