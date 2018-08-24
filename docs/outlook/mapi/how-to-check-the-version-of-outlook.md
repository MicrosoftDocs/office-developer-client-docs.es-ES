---
title: Comprobar la versión de Outlook
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 672fc380-a29b-4e99-9211-949fd5065723
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: 6369ea8948ae1996b6f88bcacd218b8dcf397306
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574695"
---
# <a name="check-the-version-of-outlook"></a><span data-ttu-id="5d18a-103">Comprobar la versión de Outlook</span><span class="sxs-lookup"><span data-stu-id="5d18a-103">Check the version of Outlook</span></span>

<span data-ttu-id="5d18a-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d18a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d18a-p101">En este tema se proporciona un ejemplo de c�digo que comprueba la informaci�n de la versi�n de las versiones instaladas de Microsoft Outlook si la versi�n instalada es Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007 o Microsoft Outlook 2003. Comprobaci�n de la versi�n de Outlook a veces es necesario para asegurarse de que un MAPI aplicaci�n llamadas elementos de la API que son compatibles con la versi�n que se est� ejecutando de Outlook.</span><span class="sxs-lookup"><span data-stu-id="5d18a-p101">This topic provides a code sample that checks version information of installed versions of Microsoft Outlook if the installed version is Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007, or Microsoft Outlook 2003. Checking the version of Outlook is sometimes necessary to ensure that a MAPI application calls API elements that are supported by the currently running version of Outlook.</span></span>

<span data-ttu-id="5d18a-p102">El siguiente ejemplo de c�digo,  `PrintOutlookVersionString`, obtiene las cadenas de versi�n completa mediante las funciones **MsiProvideQualifiedComponent** y **MsiGetFileVersion**, tal y como se declara en el archivo Msi.h en el Kit de desarrollo de Software (SDK) de Microsoft Windows.  `PrintOutlookVersionString` tambi�n devuelve un puntero a una variable de tipo Boolean que indica si se ha instalado una versi�n de 64 bits de Outlook. Para obtener informaci�n acerca de los valores esperados para las distintas partes de una cadena de versi�n de algunas versiones anteriores de Outlook, vea [c�mo determinar la informaci�n de la versi�n de Outlook](http://support.microsoft.com/kb/870929).</span><span class="sxs-lookup"><span data-stu-id="5d18a-p102">The following code sample,  `PrintOutlookVersionString`, obtains full version strings by using the **MsiProvideQualifiedComponent** and **MsiGetFileVersion** functions, as declared in the Msi.h file in the Microsoft Windows Software Development Kit (SDK).  `PrintOutlookVersionString` also returns a pointer to a Boolean variable that indicates whether a 64-bit version of Outlook is installed. For information about the expected values for the different parts of a version string for some released versions of Outlook, see [How to determine Outlook version information](http://support.microsoft.com/kb/870929).</span></span>
  
```cpp
void PrintOutlookVersionString()
{
TCHAR pszOutlookQualifiedComponents[][MAX_PATH] = {
TEXT("{E83B4360-C208-4325-9504-0D23003A74A5}"), // Outlook 2013
TEXT("{1E77DE88-BCAB-4C37-B9E5-073AF52DFD7A}"), // Outlook 2010
TEXT("{24AAE126-0911-478F-A019-07B875EB9996}"), // Outlook 2007
TEXT("{BC174BAD-2F53-4855-A1D5-0D575C19B1EA}")  // Outlook 2003
};
int nOutlookQualifiedComponents = _countof(pszOutlookQualifiedComponents);
int i = 0;
UINT ret = 0;
for (i = 0; i < nOutlookQualifiedComponents; i++)
{
DWORD dwValueBuf = 0;
LPTSTR pszTempPath = NULL;
LPTSTR pszTempVer = NULL;
bool b64 = false;
ret = pfnMsiProvideQualifiedComponent(
pszOutlookQualifiedComponents[i],
TEXT("outlook.x64.exe"),
(DWORD) INSTALLMODE_DEFAULT,
NULL,
&dwValueBuf);
if (ERROR_SUCCESS == ret)
{
b64 = true;
}
else
{
ret = pfnMsiProvideQualifiedComponent(
pszOutlookQualifiedComponents[i],
TEXT("outlook.exe"),
(DWORD) INSTALLMODE_DEFAULT,
NULL,
&dwValueBuf);
if (ERROR_SUCCESS == ret)
{
b64 = false;
}
}
if (ret == ERROR_SUCCESS)
{
dwValueBuf += 1;
pszTempPath = (LPTSTR) malloc(dwValueBuf * sizeof(TCHAR));
if (pszTempPath != NULL)
{
if (ERROR_SUCCESS == pfnMsiProvideQualifiedComponent(
pszOutlookQualifiedComponents[i],
TEXT("outlook.exe"),
(DWORD) INSTALLMODE_EXISTING,
pszTempPath,
&dwValueBuf))
{
pszTempVer = (LPTSTR) malloc(MAX_PATH * sizeof(TCHAR));
dwValueBuf = MAX_PATH;
if (ERROR_SUCCESS == pfnMsiGetFileVersion(pszTempPath,
pszTempVer,
&dwValueBuf,
NULL,
NULL))
{
printf("Path: %s\nVersion: %s\n64 bit: %s\n", pszTempPath, pszTempVer, b64?_T("true"):_T("false"));
}
}
}
free(pszTempVer);
free(pszTempPath);
}
}
}HRESULT GetOutlookVersionString(LPTSTR* ppszVer, BOOL* pf64Bit)
{
    HRESULT hr = E_FAIL;
    LPTSTR pszTempPath = NULL;
    LPTSTR pszTempVer = NULL;
    TCHAR pszOutlookQualifiedComponents[][MAX_PATH] = {
        TEXT("{E83B4360-C208-4325-9504-0D23003A74A5}"), // Outlook 2013
        TEXT("{1E77DE88-BCAB-4C37-B9E5-073AF52DFD7A}"), // Outlook 2010
        TEXT("{24AAE126-0911-478F-A019-07B875EB9996}"), // Outlook 2007
        TEXT("{BC174BAD-2F53-4855-A1D5-0D575C19B1EA}")  // Outlook 2003
    };
    int nOutlookQualifiedComponents = _countof(pszOutlookQualifiedComponents);
    int i = 0;
    DWORD dwValueBuf = 0;
    UINT ret = 0;
    *pf64Bit = FALSE;
    for (i = 0; i < nOutlookQualifiedComponents; i++)
    {
        ret = MsiProvideQualifiedComponent(
            pszOutlookQualifiedComponents[i],
            TEXT("outlook.x64.exe"),
            (DWORD) INSTALLMODE_DEFAULT,
            NULL,
            &dwValueBuf);
        if (ERROR_SUCCESS == ret) break;
    }
    if (ret != ERROR_SUCCESS)
    {
        for (i = 0; i < nOutlookQualifiedComponents; i++)
        {
            ret = MsiProvideQualifiedComponent(
                pszOutlookQualifiedComponents[i],
                TEXT("outlook.exe"),
                (DWORD) INSTALLMODE_DEFAULT,
                NULL,
                &dwValueBuf);
            if (ERROR_SUCCESS == ret) break;
        }
    }
    else
    {
        *pf64Bit = TRUE;
    }
    if (ret == ERROR_SUCCESS)
    {
        dwValueBuf += 1;
        pszTempPath = (LPTSTR) malloc(dwValueBuf * sizeof(TCHAR));
        if (pszTempPath != NULL)
        {
            if ((ret = MsiProvideQualifiedComponent(
                pszOutlookQualifiedComponents[i],
                TEXT("outlook.exe"),
                (DWORD) INSTALLMODE_EXISTING,
                pszTempPath,
                &dwValueBuf)) != ERROR_SUCCESS)
            {
                goto Error;
            }
            pszTempVer = (LPTSTR) malloc(MAX_PATH * sizeof(TCHAR));
            dwValueBuf = MAX_PATH;
            if ((ret = MsiGetFileVersion(pszTempPath,
                pszTempVer,
                &dwValueBuf,
                NULL,
                NULL))!= ERROR_SUCCESS)
            {
                goto Error;    
            }
            *ppszVer = pszTempVer;
            pszTempVer = NULL;
            hr = S_OK;
        }
    }
Error:
    free(pszTempVer);
    free(pszTempPath);
    return hr;
}

```

## <a name="see-also"></a><span data-ttu-id="5d18a-110">Vea tambi�n</span><span class="sxs-lookup"><span data-stu-id="5d18a-110">See also</span></span>

- [<span data-ttu-id="5d18a-111">Informaci�n general sobre programaci�n de MAPI</span><span class="sxs-lookup"><span data-stu-id="5d18a-111">MAPI Programming Overview</span></span>](mapi-programming-overview.md)

